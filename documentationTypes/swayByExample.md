SwayByExample Guidelines

## Target Audience
- Although this is targeted for new Sway developers the content assumes they already are somewhat familiar with basic blockchain knowledge
- Should be keeping Ethereum developers in mind when writing content

## Tone and Voice
- No personal pronouns
- Keep things granular to avoid bleeding into other topics
- Should be built off of existing 


## Formatting Example 

<H1>General Title Detailing Topic Covered</H1>

<body>Some introduction detailing what the codeblock below does</body>
<br></br>

```rust
contract;

// Comments describing the ABI
abi SwayByExample {
    
    // Comments describing the function
    #[storage(read)]
    fn some_function() -> str[20]
}

// Comments describing the storage
storage {
    some_string: str[20] = "Welcome to Sway!"
}

// Comments on implementation of the ABI for the contract
impl SwayByExample for Contract {
    #[storage(read)]
    fn some_function() -> str[20] {
        storage.some_string
    }
}
```
<H2>Relevant Project Structure</H2>

```rust
└── src
    ├── main.sw
    └── imports_library.sw
```

<prev 