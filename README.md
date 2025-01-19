# JavaScript Loose Equality Bug

This repository demonstrates a common JavaScript bug related to loose equality (==) comparisons.  The code uses `==` to check for `null`, which can lead to unexpected `NaN` results when `undefined` is passed as an argument.  The solution shows how to use strict equality (`===`) to resolve this issue.

## Bug

The `foo` function demonstrates the problem.  When `null` is passed, it correctly returns `0`.  However, when `undefined` is passed, it returns `NaN` due to the loose comparison `==` treating `undefined` and `0` as different values.

## Solution

The solution shows how to use `===` (strict equality) instead of `==` (loose equality). Strict equality requires that the values be of the same type as well as having the same value, which avoids the unintended conversion and leads to more predictable results.