# Basic Operators in Elixir

## Introduction

In this lesson we will learn about some of the basic operators in Elixir.

## Arithmetic Operators

Elixir supports the usual arithmetic operators:

```elixir
iex> 2 + 2
4
iex> 2 - 1
1
iex> 2 * 5
10
iex> 10 / 5
2.0
```

## String Concatenation

String concatenation is done with <>:
    
```elixir
iex> "foo" <> "bar"
"foobar"
```

## Comparison Operators

Comparison operators are used to compare two values:

```elixir
iex> 1 > 2
false
iex> 1 != 2
true
iex> 2 == 2
true
iex> 2 <= 3
true
```

## Boolean Operators

Elixir supports the boolean operators `and`, `or`, and `not`:

```elixir
iex> true and true
true
iex> true and false
false
iex> true or false
true
iex> false or false
false
iex> not true
false
iex> not false
true
```

### ||, && and !

Besides these boolean operators, Elixir also provides ||, && and ! which accept arguments of any type. For these operators, all values except false and nil will evaluate to true


## Comparison with Javascript

In JavaScript, the `&&` and `||` operators are used for both boolean logic and for [short-circuit evaluation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_Operators#Short-circuit_evaluation). In Elixir, the `and` and `or` operators are used for boolean logic and the `&&` and `||` operators are used for short-circuit evaluation.

```javascript
// JavaScript
true && 1
// => 1

true || 1
// => true

false && 1
// => false

false || 1
// => 1
```

```elixir
# Elixir
true and 1
# => 1

true or 1
# => true

false and 1
# => false

false or 1
# => 1
```



