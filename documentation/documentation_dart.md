# Documentation

## Comments

Write comments like sentences.

```
// Return false if name is empty.
if (name.isEmpty) return false;
```

Do not use block comments for documentation.

```
Good

greet(name) {
  // Assume we have a valid name.
  print('Hi, $name!');
}
```

```
Bad

greet(name) {
  /* Assume we have a valid name. */
  print('Hi, $name!');
}
```

## Doc Comments

# Use /// doc comments to document member types.

```
/// The number of characters in this chunk when unsplit.
int get length => ...
```

## Square brackets

# Use [] in doc comments to refer to in-scope indetifiers.

If you surround things like variable, method, or type names in square brackets, then dartdoc looks ip the name and links to the relevant API docs. Parentheses are optional, but cam make it cleare when you're referring to a method or constructor.

```
/// Similar to [Duration.inDays], but handles fractional days.
```

# The convention in Dart is to integrate that into the description of the method and highlight parameters using square brackets.

```
/// Defines a flag.
///
/// Throws an [ArgumentError] if there is already an option named [name] or
/// there is already an option using abbreviation [abbr]. Returns the new flag.
Flag addFlag(String name, String abbr) => ...
```

## Include code sample

# If your code is complex it is always a good idea to include code sample in the document as well.

```
/// Returns the lesser of two numbers.
///
/// ```dart
/// min(5, 3) == 3
/// ```
num min(num a, num b) => ...
```

# Note: You do not have to comment every method. Some method can be self explanatory.

# Resource Link.

[Dart official documentation Guide](https://dart.dev/guides/language/effective-dart/documentation)  
