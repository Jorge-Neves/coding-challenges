# Is the string uppercase?

## Prompt

Is the string uppercase?
Task
Create a method to see whether the string is ALL CAPS.

Examples (input -> output)
"c" -> False
"C" -> True
"hello I AM DONALD" -> False
"HELLO I AM DONALD" -> True
"ACSKLDFJSgSKLDFJSKLDFJ" -> False
"ACSKLDFJSGSKLDFJSKLDFJ" -> True
In this Kata, a string is said to be in ALL CAPS whenever it does not contain any lowercase letter so any string containing no letters at all is trivially considered to be in ALL CAPS.

Tags
FUNDAMENTALS STRINGS

## My attempt

```dart
  bool isUpperCase(String str) {
  for (var i = 0; i < str.length; i++) {
    if(str[i] != str[i].toUpperCase()){
      return false;
    }
  }
  return true;
}
```

## tests

```dart
import "package:test/test.dart";
import "package:solution/solution.dart";

void main() {
  group("Fixed tests", () {
    test("Testing for c", () => expect(isUpperCase('c'), equals(false)));
    test("Testing for C", () => expect(isUpperCase('C'), equals(true)));
    test("Testing for hello I AM DONALD", () => expect(isUpperCase('hello I AM DONALD'), equals(false)));
    test("Testing for HELLO I AM DONALD", () => expect(isUpperCase('HELLO I AM DONALD'), equals(true)));
    test("Testing for ACSKLDFJSgSKLDFJSKLDFJ", () => expect(isUpperCase('ACSKLDFJSgSKLDFJSKLDFJ'), equals(false)));
    test("Testing for ACSKLDFJSGSKLDFJSKLDFJ", () => expect(isUpperCase('ACSKLDFJSGSKLDFJSKLDFJ'), equals(true)));
  });
}

```

## Source

[kata](https://www.codewars.com/kata/56cd44e1aa4ac7879200010b/train/dart)
