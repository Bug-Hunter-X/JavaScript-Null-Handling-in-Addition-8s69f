# JavaScript Null Handling in Addition

This repository demonstrates a subtle bug in JavaScript related to null value handling during addition. The `foo` function uses strict equality (`===`) to check for null values, but this can lead to unexpected results when performing numerical operations.  The solution provided addresses this issue and provides a more robust approach to null handling.

## Bug Description

The initial `foo` function returns `null` if either `a` or `b` is `null`. This behavior is correct if you are explicitly checking for null values, but it's generally better to treat `null` as zero in such mathematical contexts. The bug lies in the assumption that `===` correctly handles null in numerical contexts.

## Solution

The solution uses type coercion to convert `null` values to 0 before performing the addition. This ensures that the function behaves correctly even when one or both inputs are null.