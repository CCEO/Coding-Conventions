# Mobile Development 

## Folders

 1. Inside the folder ` lib ` we **MUST** create a folder named `src ` 
 2. All the folders **MUST** be named in lowercase with `snake_case `
 3. Inside the folder ` src ` we **MUST** create another folder named `iu` where you **SHOULD** find all the views of the application
 4. Inside the folder `src` we **MUST** create another folder named `models` where you **SHOULD** find all the class of entities
 5. Add another folder named `útil` where you **SHOULD** find all the most common funtions and utilities of the application
 6. Add another folder named `widgets` where you **SHOULD** find all the widgets reusable of the application
 7. Add another folder named `service` where you **SHOULD** find all the calls to the API´s
 8. Add a file named `main.dart` which will be the main file
 9. Add a file named `routes.dart`
 10. All the files **MUST** be named in `snake_case`
 11. **Do** name types using `UperCamelCase` in the classes, enums, typedefs and type paramters. **SHOULD** capitalize the first letter of each Word
 
         class SliderMenu { ... } 
         class HttpRequest { ... }
         typedef Predicate<T> = bool Function(T value);
   
  12. **Do** name import prefixes usign `snake_case`
  
  ```php
import 'dart:math' as math;
import 'package:angular_components/angular_components'
   as angular_components;
import 'package:js/js.dart' as js;
  ```
  13. **Do** name other identifiers using `lowerCamelCase`
     
   Class members, top-level definitions, variables, parameters, and named parameters should capitalize the first letter of each word except the first word, and use no separators.
   ```php
    var item;
    HttpRequest httpRequest;
    void align(bool clearItems) {
      // ...
     }
```
  14. **Prefer** using `lowerCamelCase` for constant names. 
     In new code, use `lowerCamelCase` for constant varables, including enum values
```php
const pi = 3.14;
const defaultTimeout = 1000;
final urlScheme = RegExp('^([a-z]+):');

class Dice {
  static final numberGenerator = Random();
}
```
## Formating
1. **Do** format your code using [dartfmt](https://github.com/dart-lang/dart_style).
2. **Avoid** lines longer than 80 characters
3. **Do use** curly braces for all Flow control statements
   Doing so avoids the dangling else problem
```php
if (isWeekDay) {
  print('Bike to work!');
} else {
  print('Go dancing or read a book!');
}
```
**Exception:** When you we have an `if` statement with no `else` clause and the whole `if` statement fits on one line, you can omit the braces if you prefer:
```php
if (arg == null) return defaultValue;
```
If the body wraps to the next line, though, use braces:
```php
if (overflowChars != other.overflowChars) {
  return overflowChars < other.overflowChars;
}
```
## Documentation
### Comments
1. **Do** format comments like sentences
2. **Don´t** use block comments for documentation
   `/* lknmt*/`
3. For document classes of types ***USE** ///. 

For be able of enable [dartdoc](https://github.com/dart-lang/dart_style).
```php
/// The number of characters in this chunk when unsplit.
int get length => ...
```
4. **Do** separate the first sentence of a doc comment into its own paragraph.

  Add a blank line after the first sentence to Split it out into its own paragraph. This helps to write a tight first sentence that      summarizes the documentación. Also, tools like Dartdoc use the first paragraph as a short summary in places like lists of classes ans member

```php
/// Deletes the file at [path].
///
/// Throws an [IOError] if the file could not be found. Throws a
/// [PermissionError] if the file is present but could not be deleted.
void delete(String path) {
  ...
}
```
5. **Avoid** redundancy whit the surrounding context, 

Focus on explaning what the reader doesn´t know
**GOOD**

```php
class RadioButtonWidget extends Widget {
  /// Sets the tooltip to [lines], which should have been word wrapped using
  /// the current font.
  void tooltip(List<String> lines) {
    ...
  }
}
```
**BAD**
```php
class RadioButtonWidget extends Widget {
  /// Sets the tooltip for this radio button widget to the list of strings in
  /// [lines].
  void tooltip(List<String> lines) {
    ...
  }
}
```

6. **Prefer** starting function or method comments with third-person verbs

The doc comment focus on what the code does
```php
/// Returns `true` if every element satisfies the [predicate].
bool all(bool predicate(T element)) => ...

/// Starts the stopwatch if not already running.
void start() {
  ...
}
```

7. **PREFER** starting variable, getter, or setter comments with noun phrases

The comment should stres what the property is, avoid having a doc comment on both the setter and the getter, as DaryDoc will show only one (getter).

```php 
/// The current day of the week, where `0` is Sunday.
int weekday;

/// The number of checked buttons on the page.
int get checkedCount => ...
```
8. **PREFER** starting library or type comments with noun phrases.
```php
/// A chunk of non-breaking output text terminated by a hard or soft newline.
///
/// ...
class Chunk { ... }
```
9. **CONSIDER** including code simples in doc comments

```php 
/// Returns the lesser of two numbers.
///
/// ```dart
/// min(5, 3) == 3
/// ```
num min(num a, num b) => ...
```
10. **Do** use square brackets in doc comments to refer to in-scope identifiers.

If we sorround things like variable, method or type names in square brackets, then dartdoc looks up the name and links to the relevant API docs.
Parentheses are optional, but can ake it clear when we are referring to a method or constructor

```php
/// Throws a [StateError] if ...
/// similar to [anotherMethod()], but ...
```

To link to a member of specific class, use the class name and member name, separated by a dot

```php
/// Similar to [Duration.inDays], but handles fractional days.`
```

The dot syntax can also be used to refer to named constructors. For the unnamed constructor, put parentheses after the class name:

```php
/// To create a point, call [Point()] or use [Point.polar()] to ...`
```

11. **DO** use prose to explain parameters, return values, and exceptions.

Other languages use verbose tags and sections to describe what the parameters and returns of a method are.
**BAD**
```php
/// Defines a flag with the given name and abbreviation.
///
/// @param name The name of the flag.
/// @param abbr The abbreviation for the flag.
/// @returns The new flag.
/// @throws ArgumentError If there is already an option with
///     the given name or abbreviation.
Flag addFlag(String name, String abbr) => ...
```
The convention in Dart is to integrate that into the description of the method and highlight parameters using square brackets.
**GOOD**
```php
/// Defines a flag.
///
/// Throws an [ArgumentError] if there is already an option named [name] or
/// there is already an option using abbreviation [abbr]. Returns the new flag.
Flag addFlag(String name, String abbr) => ...
```
12. **Use** markdown formatting in ypu doc comments and dardoc will proces it accordingly using the markdown package
13. **PREFER** brevity
14. **AVOID** abbreviations and cronyms unless they are obvious




