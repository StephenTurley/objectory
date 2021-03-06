#Recent change notes

###0.3.21

- Domain model autogeneration from simple proto-model (models are backward compatible)
- Autogeneration of helper schema classes, for safe fields choosing for `find` and `findOne` queries
- Examples and test adopted for new features

###0.3.20

- Fix for [issue 65](https://github.com/vadimtsushko/objectory/issues/65). Added test testPersistentListWithEmbeddedObjects

###0.3.19

- BugFix in ObjectoryServerImpl, objectory server port changed in samples and tests to avoid conflict with pub serve

###0.3.18

- Update core dependencies to 0.10.0 and up

###0.3.16

- bugfix in ObjectoryServerImpl. Addressed [issue 64](https://github.com/vadimtsushko/objectory/issues/64)

###0.3.15

- `get` method added to objectory collection
- Objectory `addToCache` method made private 
- Quick tour somewhat updated
- Changelog moved to root in accordance with pub site preferences
- some refactoring in objectory initialization
- `fetch` method of PersistentObject returns future of itself now
- previously deprecated method `dbType` on PersistenObject removed
- `isFetched` getter added to PersistentObject (false for shallow proxy)


###0.3.14

- Bug fix: PersistentObject map setter was setting id to null
- Name change: Objectory datamapDecorator renamed to dataMapDecorator
- dataListDecorator added to Objectory 
- Package prepared to Dart 1.0

###0.3.13

- Upgrade for Dart SDK version 0.1.2.0_r29782. Gwt_Contacts sample is broken, waiting for fix in original 
dart-polyhmer-dart-examples
 
###0.3.12

- Port of polymer GwtContacts sample added 
- Bugfix to PersistentObject save method
- Many minor changes
- dbType deprecated, use collectionName instead.

###0.3.11

- Added datamapDecorator property to Objectory, so PersistentObject's data map may be substituted by arbitrary
map-like object upon creation. For example Web-UI application may configure Objectory to make PersistenObject observable by:
`objectory.datamapDecorator = (Map map)=>toObservable(map);` 

###0.3.10

- Bugfix and test for situation when save operation on PersistentObject without dirty fields (should be no-op)
actually set all its properties to null

###0.3.9

- Bugfix for issue https://github.com/vadimtsushko/objectory/issues/52. Case added in tests
- Tests refactored

###0.3.8

- Objectory now use field level updates (update with $set operator) by default. This shoud greatly reduses problems 
with concurrent updates. Old mode can be toggled by attribute useFieldLevelUpdate

###0.3.7

-Small changes in query builder. Better error handling in open connection 
(pull requests from kaisellgren and izaera respectively) 

###0.3.5-0.3.6

- Small changes, bugfixes in query builder


###0.3.4

- Bugfix for remove operation in objectory_server (was not implemented)

###0.3.3

- Upgrade for bson 0.1.5. json_ext dependenvy removed.


###0.3.2

- Query API supports AND and OR operators


###0.3.1

- Bugfix in WebSocket VM implementation.

###0.3.0

- Modelling API revamped. Classes in modelling designated by Type not by string names.
- Querying API revamped, more closely followed to mongo_db and mongo_dart patterns.

###0.2.2

- PersistentObject got getPersistentList method as preferred way to define List properties in models.  

###0.2.1

- match in QueryBuilder go named instead of positional parameters 
- where in QueryBuilder deprecated in favour of jsQuery
- range in QueryBuilder deprecated in favour of inRange
- test for match added
- test for jsQuery added

###0.2.0

- Client/Server communication moved from JsonExt to Bson (using new cross-platform version of bson)
- Bugfix on browser side - findOne still was using cache.

###0.1.9

- Change in dependencies - bson library separated from within mongo_dart 

###0.1.8

- Upgrade to Dart SDK version 0.5.0.1_r21823
- find() and findOne() always get objects from Db (If objects exists in cache they are replaced by fresh ones from Db) 

###0.1.7

- PersistentList inherit from ListBase. No more notimplemented methods and type warnings. 

###0.1.6

- Upgrade for Dart SDK version 0.4.7.5_r21658 (post M4)

###0.1.5

- Count() method implemented on all platforms

###0.1.4

- Upgrade for M4 changes
- Obectory server now does not log messages my default, verbosity switched by command line parameter --verbose

###0.1.3

- Bugfixes for PersistentObject methods: contains, indexIf, lastIndexOf
- save and remove methods returns Future (consistently with Objectory save and return)
- supported Dart SDK version 0.4.5.1_r21094

###0.1.0

- Support of dart:io version 2. (Stream-based).
- fetchLinks method of QueryBuilder (With it PersistentObjects in resultset of findOne and find prefetch linked objects)

###0.0.11

- Support for near and within geospatial queries in QueryBuilder (Thanks to Jesse https://github.com/FreakTheMighty)

###0.0.10

- Support for limit and skip operation in QueryBuilder.

###0.0.8

- Ready for M3, run in version 0.3.1_r17328

###0.0.7

- dart.js bootstrap file is moving to pub

###0.0.6

- Minor fixes
- Cleared all warnings from DartEditor
- Pubspec refers to dart_mongo from pub.dartlang.org
- Local_objectory_tests broken due to lawndart errors.

###0.0.5

- minor fixes
- sdk dependencies changed to pub.dartlang.org

###0.0.4

- Changes reflecting dart lib changes - methods to getters, such as Map.getKeys() and so on
