Bright Inventions Objective-C Style Guide
=========================================

A set of coding conventions we use at [Bright Inventions](http://brightinventions.pl) for iOS projects. 

Based upon https://github.com/NYTimes/objective-c-style-guide and "Effective
Objective-C 2.0" by Matt Galloway


## Minimize Importing Headers in Headers

Prefer forward declaration (@class, @protocol) to #include in header files. It minimizes coupling and speeds up compile time significantly. 


## Dot-Notation Syntax

Dot-notation should **always** be used for accessing and mutating properties. Bracket notation is preferred in all other instances. 

## Prefer Literal Syntax over the Equivalent Methods

Whenever possible initialize NSNumbers, NSArrays, NSDictionaries using literal syntax. 

NSArray *animals = @[@"cat", @"dog", @"mouse", @"badger"];
NSDictionary *personData = @{
      @"firstName" : @"Matt",
      @"lastName" : @"Galloway",
      @"age" : @28
};

NSNumber *doubleNumber = @3.14159;
NSNumber *boolNumber = @YES;


When accessing array or dictionary elements also prefer literal syntax:
NSString *dog = animals[1];
NSString *lastName = personData[@"lastName"];


## Prefer Typed Constants to Preprocessor #define













