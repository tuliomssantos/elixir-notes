# Atoms and Tuples

## Introduction

In this lesson we will learn about two of the basic data types in Elixir: atoms and tuples.

## Atoms

An atom is a constant whose name is its value. Atoms are often used to represent things; for example, we can have the atom `:ok` to represent a successful operation, `:error` to represent an error, and so on.

Atoms are also used to reference modules and their functions, as we will see in later exercises.

```elixir
iex> :atom
:atom
```

Atoms are also used to reference modules and their functions, as we will see in later exercises.

```elixir
iex> :atom == :atom
true
iex> :atom === :atom
true
```

## Tuples

Tuples are similar to lists, but are stored contiguously in memory. This makes accessing their length fast, but accessing their elements (by index) slow.

Tuples are defined with curly braces:

```elixir
iex> {:ok, "Hello"}
{:ok, "Hello"}
```

Tuples are also used to return additional information from functions. For example, `File.read/1` returns a tuple `{:ok, contents}` where `contents` is a binary representing the contents of the file, or `:error` if there was an error:

```elixir
iex> File.read("path/to/existing/file")
{:ok, "... contents ..."}
iex> File.read("path/to/unknown/file")
:error
```

### Common Use Cases for Tuples

Tuples are often used as return values from functions. For example, the `File.read/1` function returns a tuple `{:ok, contents}` where `contents` is a binary representing the contents of the file, or `:error` if there was an error:

```elixir
iex> File.read("path/to/existing/file")
{:ok, "... contents ..."}
iex> File.read("path/to/unknown/file")
:error
```

## Exercises

### 1. Create an atom

Create an atom named `:elixir`.

```elixir   
iex> :elixir
:elixir
```

### 2. Create a tuple

Create a tuple with the atom `:ok` and the integer `42`.

```elixir
iex> {:ok, 42}
{:ok, 42}
```

### 3. Create a tuple with a keyword list

Create a tuple with the atom `:ok` and the keyword list `name: "One"`.

```elixir
iex> {:ok, name: "One"}
{:ok, [name: "One"]}
```

### 4. Create a tuple with a map

Create a tuple with the atom `:ok` and the map `%{name: "One"}`.

```elixir
iex> {:ok, %{name: "One"}}
{:ok, %{name: "One"}}
```

### 5. Create a tuple with a list

Create a tuple with the atom `:ok` and the list `["One"]`.

```elixir
iex> {:ok, ["One"]}
{:ok, ["One"]}
```

### 6. Create a tuple with a tuple

Create a tuple with the atom `:ok` and the tuple `{:error, "One"}`.

```elixir
iex> {:ok, {:error, "One"}}
{:ok, {:error, "One"}}
```

### 7. Create a tuple with a function

Create a tuple with the atom `:ok` and the function `fn -> "One" end`.

```elixir

iex> {:ok, fn -> "One" end}
{:ok, #Function<20.126501267/0 in :erl_eval.expr/5>}
```

### 8. Create a tuple with a PID

Create a tuple with the atom `:ok` and the PID of the current process.

```elixir

iex> {:ok, self()}
{:ok, #PID<0.108.0>}
```

### 9. Create a tuple with a reference

Create a tuple with the atom `:ok` and the reference of the current process.

```elixir

iex> {:ok, make_ref()}
{:ok, #Reference<
    0.1705680183.2
    >}
```

### 10. Create a tuple with a port

Create a tuple with the atom `:ok` and the port of the current process.

```elixir

iex> {:ok, spawn_link(fn -> :timer.sleep(1000) end)}
{:ok, #Port<0.3>}
```

### 11. Create a tuple with a bitstring

Create a tuple with the atom `:ok` and the bitstring `<<1, 2>>`.

```elixir

iex> {:ok, <<1, 2>>}
{:ok, <<1, 2>>}
```

### 12. Create a tuple with a float

Create a tuple with the atom `:ok` and the float `1.0`.

```elixir

iex> {:ok, 1.0}
{:ok, 1.0}
```

