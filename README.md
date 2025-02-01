# lexy-language

[View demo!](https://lexy-language.github.io/lexy-demo/)

# Philosophy

Lexy is a DSL (Domain Specific Language) designed by Tim Cools to describe tax laws. Currently, tax laws are published and updated with textual descriptions, sometimes ambiguous and open for interpretation. 
The tax system in most countries favors people with a lot of money who can pay expensive specialists to learn how to avoid paying taxes. This contributes to widening income and wealth inequality.

- What: Executable tax laws published by governments
- Who: Used by lawmakers, scientific researchers, tax specialists, IT companies implementing tax laws,and  students.
- Why: Consistency and transparency: we believe tax returns should be published in public (as in some countries in Scandinavia)


Besides describing tax laws, the language can be used to implement all kinds of calculations. 

Advantages:
- Computer language independent: Calculations can be integrated into many existing and new applications regardless of the language it is written in. 
- Real-time execution: The calculations can be changed and executed, without recompiling the main application. 
- Simple and readable: the goal is to keep the language as simple as possible. It should be readable by advanced (non-developer) spreadsheet users. 
- Transparency: during the execution of a lexy script every decision is logged
- Versioning: 

Hosting
- Public portal/ Local IDE
- Any host programming language: currently dotnet and typescript/javascript
- Blockchain: was the initial idea. The main problem a blockchain solves is the decentralization of trust. While the lack of a central authority can be useful in some cases, this is only necessary when multiple organizations can't fully trust each other. We believe that the government of nations should be able to trust itself, and should be trusted by it's citizens. So storing and executing tax scripts would be an irresponsible use of computing and storage resources. A blockchain that publicly publishes immutable lexy scripts, executes them and publishes the results in public might have different use cases though.
- GPU

# How to contribute?

I'm looking for a manager who can manage the development and community (discord)

- Tax specialists with IT knowledge, developers with Tax knowledge
- Government
- Developers withan  interest in parsers and compilers
- Sponsors/Companies: sponsor developer time

# Syntax

## Function

`Function: HelloWorld`

## Enum

```
Enum: MaritalStatus
  Single
  Married
```

## Type
## Table
## Scenario

# Language Specifications

## Scenario

# Setup

## Run locally

Each parser shou
[lexy-dotnet](https://github.com/lexy-language/lexy-dotnet) or [lexy-typescript](https://github.com/lexy-language/lexy-typescript) run these specfications to validate the outcome in their automated tests.


## Known improvements

- [ ] More scenarios for side cases and alternative branches of the current parser. Code coverage reveals validations, ... which are not verified in the language specifications yet

## Future ideas

- [ ] Tables: support of csv and/or json tables
- [ ] Syntax: support identifiers with underscore '_' (double underscores should not be allowed as it is reserved for system functions and variables)
- [ ] Syntax: support **for** loop
- [ ] Syntax: support **while** loop
- [ ] Syntax: support of arrays
- [ ] Versioning: document versioning strategy for lexy scripts (branches) and how to reuse scripts (by using submodules) 
- [ ] Versioning: document versioning strategy for **lexy-langage** and its dependencies


# Implementations notes

## Submodules

**lexy-language** is included as a git submodule. 
- **lexy-language** is used in the automated tests to 
ensure that the parser and compiler are running against the latest lexy language specifications.

To update the submodule to the latest version: `cd tests/lexy-language/ && git pull` (ensure you pull the right branch is you're implementing a new branch of lexy-language)

## Circular references
`import type`
