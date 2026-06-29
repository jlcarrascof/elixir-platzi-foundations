# Basic data

## Anonymous functions

```elixir
add = fn a, b -> a + b end
```

```elixir
add.(1, 2)
```

```elixir
is_function(add)
```

```elixir
is_function(add, 1)
```

```elixir
is_function(add, 2)
```

```elixir
double = fn a -> add.(a, a) end
double.(2)
```

```elixir
x = 42
(fn -> x = 0 end).()
x
```

## Lists

```elixir
[1, 2, 3, true]
```

```elixir
length [1, 2, 3]
```

```elixir
[1, 2, 3] ++ [4, 5, 6]
```

```elixir
[1, true, 2, false, 3] -- [true, false]
```

```elixir
[1, 2, true, false, 3, true] -- [false, true]
```

```elixir
list = [1, 2, 3]
hd(list)
```

```elixir
tl(list)
```

```elixir
hd([])
```

```elixir
tl([])
```

## Tuples

```elixir
{:ok, "hello"}
```

```elixir
tuple_size({:ok, "hello"})
```

```elixir
tuple = {:ok, "hello"}
elem(tuple, 1)
```

```elixir
put_elem(tuple, 1, "world")
```

```elixir
tuple
```
