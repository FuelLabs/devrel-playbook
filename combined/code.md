# Code samples

Code examples are one of the most important resources when referencing the correct syntax and style. For additional details on how to format and embed code within text, command-line syntax, and placeholders, take a look at the the resources below. 

## Three general rules
1. Only use spaces to indent code never tabs
2. Lines should not exceed `80` characters

<table>
<tr>
<td> Recommended ✅</td>
</tr>
<tr>
<td>

```rust
contract;

abi HelloModular {
    #[storage(read)]
    fn greet() -> str[90];
}

storage {
    greet: str[90] = "This line should be wrapping because it is over 80 characters long"
}

...

```

</td>

</tr>
<tr>
</tr>
</table>

3. Use three dots and no spaces to replace omitted code ( ... )
   - If the omitted code is one or more lines long replace with its own line
<table>
<tr>
<td> Recommended ✅</td> <td> Not Recommended ❌</td>
</tr>
<tr>
<td>

```rust
contract;

...

impl HelloModular for Contract {
    #[storage(read)]
    fn greet() -> str[16] {
        storage.greet
    }
}
```

</td>

<td>

```rust
contract; . . .

impl HelloModular for Contract {
    #[storage(read)]
    fn greet() -> str[16] {
        storage.greet
    }
}
```

</td>
</tr>
<tr>
</tr>
</table>