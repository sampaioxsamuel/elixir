# Atoms

```elixir
:banana
:banana == "banana"
# false

:banana == :banana
# true

true == :true
# true, bc true is an atom in elixir

is_atom(:banana)
```

# Lists

```elixir
# its a linked list, so we can´t have direct access to the elements
list = [1, 2, 3]

list2 = [1, 2, "string"]

list3 = [1, 2, 3] ++ [4, 5, 6]
# [1,2,3,4,5,6]

list4 = [1, 2, 3] -- [4, 5, 6]
# [1,2,3]

list5 = [1, 2, 3] -- [1, 3]
# [2]

# Access the head/first element of the list
hd([1, 2, 3])
# [1]

# Access the tale/any element that is not the head

tl([1, 2, 3])
# [2,3]

# or
[head | tail] = [1,2,3,4]

head
# 1

tail
# 2,3,4
```


# Tuple

```elixir
tuple = {1, 2, 3}

elem(tuple, 2)
# 3

x = {1, 2, 3}
put_elem(x, 2, "abacaxi")
# {1,2, "abacaxi"}
```

# Maps

```elixir
map = %{a: 1, b: 2, c: 3}

x = %{a: "hello", b: 1}
x.a
# "hello"

z = %{"a" => "hello", "b" => 2}
z["a"]
# "hello"

x = %{a: 1, b: 2, c: 3}

new_map = %{x | b: 5}
# {a: 1, b: 5, c: 3}
# by doing this "%{x | old_key: new_value}" we will keep the others but change a especific key value
```

# Pattern Matching

```elixir
[a, b, c] = [1, 2, 3]
# a = 1
# b = 2
# c = 3

%{a: value} = %{a: 100, b: 500}
# value = 100

# Pin

^x = 4
# 4

^x = 10
# Match error because `x` is already declared
```