Humanitarian-Activity-Streams
==============================

Humanitarian Activity Streams (HAS) is external vocabulary for [Activity Streams](http://activitystrea.ms/) schema which includes object definitions specific to crisis response.  An open source, community developed standard that will allow web and mobile applications to share humanitarian worker's activities to improvbe coordiation and accountability.


## Activity Streams

Activity Streams is a format for representing events or activities in
a social network or in *collaborative software*. It's being written in
[JSON](http://json.org/) format.

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

## Humanitarian Activity Streams (examples)

| Objects  Types      | Objects  Types          | Description             |
| -------------       |:-------------:| -----:|
| Disaster          | disaster | $1600 |
| Assesment          | assessment | $1600 |
| Beneficiary         | centered      |   $12 |
| Distribution      | are neat      |    $1 |
| Office           | centered      |   $12 |
| Warehouse       | are neat      |    $1 |
| Security Incident            | centered      |   $12 |
| Training      | are neat      |    $1 |
| IDP Camp            | centered      |   $12 |
| Shelter  | are neat      |    $1 |


An example of an Activity Streams activity:

    {
        "id": "c1kj334jii",
        "actor": {
            "id": "acct:finan@reliefcloud.example",
            "displayName": "Dan Finan",
            "objectType": "person",
            "url": "http://reliefcloud.example/finan"
        },
        "verb": "read",
        "object": {
            "id": "http://reliefweb.int/disaster/tc-2013-000139-phl",
            "name": "Typhoon Haiyan - Nov 2013"
            "objectType": "disaster"
        },
        "target": {
            "id": "http://reliefweb.int/",
            "name": "ReliefWeb"
            "objectType": "page"
        },
        "published": "1973-01-01T00:00:00"
    }


The activity would read:  'Dan Finan read about Typhoon Haiyan on RelifWeb'

This activity has an `id` to uniquely identify it, an `actor`, a
`verb`, and an `object`. It also has a publication timestamp,
`published`. The actor is a "person" with a name and an `id` that is
an "acct:" URI, as well as an `url` of a profile page. The object is a
"disaster", as defined on RelifWebs API and the 

The activity streams specification is long; there are also several
extensions that pump.io supports. The
[Activity Base Schema](http://activitystrea.ms/specs/json/schema/activity-schema.html)
lists some common object types and verbs.

It's possible to make new object types and new verbs by using full
URIs for the `objectType` or `verb` property. Unknown object types or
verbs will be stored but won't cause side-effects.

