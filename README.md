[![Build Status](https://travis-ci.org/pardom/ActiveAndroid.png?branch=master)](https://travis-ci.org/pardom/ActiveAndroid) [![Stories in Ready](https://badge.waffle.io/pardom/ActiveAndroid.png)](http://waffle.io/pardom/ActiveAndroid)
# ActiveAndroidPlus

Fork from ActiveAndroidRx (vicpinm repository) version 3.1.5

- ActiveAndroidRx : Reactive queries with SQLBrite from Square
- UPDATE onConflictAction
- in() andIn() orIn() methods in From class (in() and andIn() are same method)
- Manipulate last transaction in static mode

## Usage

ActiveAndroidRx:

    RxSelect.from(MyEntity.class).where(...).execute().subscribe(myEntitiesList -> ...);

UPDATE OnConflictAction:

    @Column(... onConlictAction=ConflictAction.UPDATE)

Transaction

    ActiveAndroid.beginTransaction();         // Start a new transaction. Return a SQLBrite.Transaction
    ActiveAndroid.commitTransaction();        // Mark last transaction as successful and end it one
    ActiveAndroid.setTransactionSuccessful(); // Mark last transaction as successful
    ActiveAndroid.endTransaction();           // End last transaction (rollback if no marked as successful)
    ActiveAndroid.getLastTransaction;         // Get last SQLBrite.Transaction if not ended

## Download

Grab via Gradle:
```
groovy
repositories {
    maven { url "https://jitpack.io" }
}

compile 'com.github.sarigue:activeandroidplus:master'
```
or
```
compile 'com.github.sarigue:activeandroidplus:(commit ID)'
```


## Documentation

* [Getting started](http://github.com/pardom/ActiveAndroid/wiki/Getting-started)
* [Creating your database model](http://github.com/pardom/ActiveAndroid/wiki/Creating-your-database-model)
* [Saving to the database](http://github.com/pardom/ActiveAndroid/wiki/Saving-to-the-database)
* [Querying the database](http://github.com/pardom/ActiveAndroid/wiki/Querying-the-database)
* [Type serializers](http://github.com/pardom/ActiveAndroid/wiki/Type-serializers)
* [Using the content provider](http://github.com/pardom/ActiveAndroid/wiki/Using-the-content-provider)
* [Schema migrations](http://github.com/pardom/ActiveAndroid/wiki/Schema-migrations)
* [Pre-populated-databases](http://github.com/pardom/ActiveAndroid/wiki/Pre-populated-databases)
* [Running the Test Suite](https://github.com/pardom/ActiveAndroid/wiki/Running-the-Test-Suite)

## License

[Apache Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

    Copyright (C) 2010 Michael Pardo

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

## Contributing

Please fork this repository and contribute back using [pull requests](http://github.com/pardom/ActiveAndroid/pulls).

Any contributions, large or small, major features, bug fixes, unit tests are welcomed and appreciated but will be thoroughly reviewed and discussed.

You can run the test suite by following the instructions on the [Running the Test Suite](https://github.com/pardom/ActiveAndroid/wiki/Running-the-Test-Suite) Wiki page.


## Author

Francois Raoult | http://francois.raoult.name

Víctor Manuel Pineda Murcia | http://vicpinm.github.io/ActiveAndroidRx/

Original Project: 
Michael Pardo | www.michaelpardo.com | www.activeandroid.com
