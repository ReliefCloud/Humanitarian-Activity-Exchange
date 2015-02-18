Humanitarian-Activity-Streams
==============================

Humanitarian Activity Exchange (HAX) is set of json schema that defines humanitarian activities with location data (GeoJson) for applications aiming to improve the coordination among relief response workers

pump.io API is based on three major technologies:

- [Activity Streams](http://activitystrea.ms/) for data format
- [OAuth 1.0](http://tools.ietf.org/html/rfc5849)
- [Web Host Metadata](http://tools.ietf.org/html/rfc6415)

There are some bits of other things floating around, like:

- [OpenID Connect Dynamic Client Registration](http://openid.net/specs/openid-connect-registration-1_0.html)
- [Dialback Access Authentication](http://tools.ietf.org/html/draft-prodromou-dialback-00)

Finally, the API uses
[REST](http://en.wikipedia.org/wiki/Representational_state_transfer)-ish
principles and follows some of the patterns, but none of the actual
requirements, of [The Atom Publishing Protocol](http://tools.ietf.org/html/rfc5023).

## TL;DR

Here's the quick start version of the API:

* Register a new OAuth client by posting to the client registration endpoint.
* Use OAuth 1.0 to get an OAuth token for the user.
* Post to the user's activity outbox feed to create new
  activities. These can create new content, respond to existing
  content, or modify the social graph.
* Read from the user's activity inbox to see stuff that other people
  have sent to them.

## Activity Streams

Activity Streams is a format for representing events or activities in
a social network or in collaborative software. It's a
[JSON](http://json.org/) format (at least, we only support the JSON
format), meaning that on the wire data looks like JavaScript literals.

Activity Streams data includes a few different kinds of things:

* objects: These represent real or digital objects. Every object has
  an `objectType` property; some common object types are "person",
  "note", "image", "place". There are some standard properties that
  all object types support, like `displayName` for an easy-to-use
  short text name, or `content` for HTML content representing the
  object. Some types have unique properties, like a "place", which has
  a `position` and an `address`. Every object has a unique `id`,
  which is a
  [URI](http://en.wikipedia.org/wiki/Uniform_resource_identifier) that
  identifies that object globally.
* activities: An activity is something that happened. It's like a
  sentence; it has an `actor`, who did the thing, a `verb` that is
  what happened, and an `object` which is what it happened
  to. Activities can also have some other properties, like a
  `location` or a `target`. Activities also have an `id` property that
  uniquely identifies the activity.
* collections: These are ordered lists of activities.

An example of an Activity Streams activity:

    {
        "id": "http://coding.example/api/activity/bwkposthw",
        "actor": {
            "id": "acct:bwk@coding.example",
            "displayName": "Brian Kernighan",
            "objectType": "person",
            "url": "http://coding.example/bwk"
        },
        "verb": "post",
        "object": {
            "id": "http://coding.example/api/note/helloworld",
            "content": "Hello, World!"
            "objectType": "note"
        },
        "published": "1973-01-01T00:00:00"
    }

This activity has an `id` to uniquely identify it, an `actor`, a
`verb`, and an `object`. It also has a publication timestamp,
`published`. The actor is a "person" with a name and an `id` that is
an "acct:" URI, as well as an `url` of a profile page. The object is a
"note".

The activity streams specification is long; there are also several
extensions that pump.io supports. The
[Activity Base Schema](http://activitystrea.ms/specs/json/schema/activity-schema.html)
lists some common object types and verbs.

It's possible to make new object types and new verbs by using full
URIs for the `objectType` or `verb` property. Unknown object types or
verbs will be stored but won't cause side-effects.

