
# Headings and Titles

When crafting developer documentation, it is crucial to employ headers and titles to set the purpose of the page. Try to keep headings and titles **clear** and **concise** as they are the most useful for documentation navigation.

## Five general rules

1. Use sentence case for headings and titles.
   - For example `Smart contract deployment` should be used not `Smart Contract Deployment`
2. Incorporate abbreviations within the description after it is used in a heading
  - For example `FVM` (`Fuel Virtual Machine`)
3. Only **ONE** `h1` header per page
4. If possible, avoid duplicating the exact page title in the heading
5. Refrain from including links in headings

<table>
<tr>
<td>Guidance</td> <td> Recommended ✅</td> <td> Not Recommended ❌</td>
</tr>
<tr>
<td>
Use <a href="https://en.wikipedia.org/wiki/English_verbs#Base_form">baed form verbs</a> and avoid using -ing in tasked based headings 
</td>
<td>

```md
# Write a Sway smart contract
```

</td>

<td>

```md
# Writing a Sway smart contract
```

</td>
</tr>
<tr>
<td>Use 
    <a href="https://en.wikipedia.org/wiki/Noun_phrase">noun phrase</a> without -ing in concept based headings
</td>
<td>

```md
# Calling Contracts
```

</td>

<td>

```md
# Contract Calls
```

</td>
</tr>
</table>

## Heading Hierarchy

- Headings must follow the previous levels 
  - For example and `h2` heading can ONLY be used after an `h1` heading
  - Do not skip to the `h3` tag 

<table>
<tr>
<td> Recommended ✅</td> <td> Not Recommended ❌</td>
</tr>
<tr>
<td>

```md
# Sway Program Types

There are many different types of Sway programs including, contracts, predicates, scripts and libraries.

## Predicates
```

</td>

<td>

```md
# Sway Program Types

There are many different types of Sway programs including, contracts, predicates, scripts and libraries.

### Predicates

```

</td>
</tr>
<tr>
</tr>
</table>

- Information must be provided to support the heading
  - Do not skip from one heading to the next

<table>
<tr>
<td> Recommended ✅</td> <td> Not Recommended ❌</td>
</tr>
<tr>
<td>

```md
## Sway contract test

A Cargo generated template will be used to test and validate the Sway smart contract in the following steps.

### Generate default test harness
```

</td>

<td>

```md
## Sway contract test

### Generate default test harness

```

</td>
</tr>
<tr>
</tr>
</table>
