# EIP-2535 Multi-Facets Proxy Factory [![Linux Build](https://github.com/G7DAO/multi-faceted-proxy-factory/actions/workflows/Linux-npx-hardhat-test.yml/badge.svg)](https://github.com/G7DAO/multi-faceted-proxy-factory/actions/workflows/Linux-npx-hardhat-test.yml)

EVM Compatible Smart Contract system that will create Audited On-Chain EIP-2535 
Smart Contract Facets that can be used as blueprints that developers can use to build EIP-2535 Smart Contracts.  

[EIP-2535: Diamonds, Multi-Facet Proxy](https://eips.ethereum.org/EIPS/eip-2535) 

## Summary
The EIP-2535 smart contracts are extensible without having to redeploy existing functionality. 
Parts of a diamond can be added / replaced / removed while leaving other parts alone. 
They can be immutable or mutable. The EIP-2535 Standard enables people to write 
smart contracts with virtually no size limit, standardizes contract interfaces and 
makes interoperability easier to achieve.

The Multi-Faceted Proxy Factory is the base Proxy Contract & Factory that holds all the EIP-2535 deployed 
smart contract facets.

The Proxy Contract exists on chain and is not upgradeable once deployed but serves as Proxy for any number
of EIP-2535 Facets contracts that are upgradeable.

This project will also house sample audited EIP-2535 Smart Contracts.

The system also uses Mocha and typescript for writing tests.

## Problem
The problem experienced by the greatest number of Web3 Developers in the development of Web3 
products as cited in the [G7 Industry Report](#) was a lack of off-the-shelf smart contracts that are 
commonly used. The contracts should be easy to find, should be queryable by 
common use cases, should be secure and should be battle tested. 

## Solution
The creation of hundreds of On-chain EIP-2535 Diamond Facets that act as battle tested function libraries. 
These functions and their addresses are stored in an to generate a database for the to be made available to
the Diamond Blueprinter. 

The Diamond Blueprinter can then organize these functions as commonly used contracts that meet common use
cases yet still allows the developer to further customize the contract to meet their specific 
needs.   

### Facet
A Facet is simply an On-Chain Library of Functions.

Facets are Reusable and Composable. A deployed facet can be used by any number of diamonds.

Different combinations of facets can be used with different diamonds.

It is possible to create and deploy a set of facets that are reused by different diamonds over time.

The ability to use the same deployed facets for many diamonds reduces deployment costs.

A limitation is that two external functions with the same function signature can’t be added to a diamond at
the same time because a diamond, or any contract, cannot have two external functions with the same function 
signature.

A facet defines external functions and can define or use internal functions, libraries, and state variables.

A facet can declare state variables in structs. Each struct is given a specific position in contract storage. 
This technique is called Diamond Storage.


## Getting Started
The repository will consist of the following functionality:
* **50 (on-chain) EIP-2535 Diamond Facets** that contain commonly used, battle tested functions that would 
be useful for creating a prototype.
* **Testing Suite** for facets. Incorporate the [Bugout Facet Inspector](https://github.com/bugout-dev/inspector-facet) and Slither.
* **Storage Mechanism** for all functions that are used in the facets. Store should be a data store that is friendly to
recommendation engines.
* **Storage Mechanism** for additional metadata required for contract assembly. Correlate metadata with 
stored functions.
* **Pre-assembled** smart contracts that can be used for common use cases. Make them searchable.
* **Basic platform** with rest / graphql api endpoints using the G7 Microservice Platform Boilerplate
* **Api endpoints** that are needed to generate the required payloads.

## Prerequists for Compiling and Running the Code
* **Node JS v14+**
* **npm v6+**
* **clang or other host C++ compiler for some npm packages**
* **git**
* **Visual Studio Community, Jetbrains IntelliJ or other code Editor**
* **Meta Mask (optional)**
* **Infura.io account (optional, but recommended)**

## FAQ
**Who will use this?**
* Smart Contractor developers who are looking for boilerplate EVM compatible contracts.
* Smart Contractor developers who are looking for upgradeable, extensible EVM compatible contracts. 
* Smart Contractor developers who are looking for a secure way to develop EVM compatible contracts.
* Smart Contractor developers who are looking for an easy way to build EVM compatible contracts.
* Smart Contractor developers who are looking for an easy way to learn EIP-2535 Diamond contracts.
* Game developers who are looking for an extensible contracts that can grow with their game.
 
**What problem does this really solve?**
* **A single address for unlimited contract functionality.** Using a single address for contract functionality makes deployment, testing and integration with other smart contracts, software and user interfaces easier.
* **Your contract exceeds the 24KB maximum contract size.** You may have related functionality that it makes sense to keep in a single contract, or at a single contract address. A diamond does not have a max contract size.
* **A diamond provides a way to organize contract code and data.** You may want to build a contract system with a lot of functionality. A diamond provides a systematic way to isolate different functionality and connect them together and share data between them as needed in a gas-efficient way.
* **A diamond provides a way to upgrade functionality.** Upgradeable diamonds can be upgraded to add/replace/remove functionality. Because diamonds have no max contract size, there is no limit to the amount of functionality that can be added to diamonds over time. Diamonds can be upgradeable or immutable. It is also possible to make an upgradeable diamond and then at a later time remove its upgrade capability.
* **Automated assembly, testing and launching of EIP-2535 Diamond Contracts**
* **A library of existing, audited, on-chain, EIP-2535 Diamonds Facets**

**Is this just another walled garden designed to monetize something that's freely available?**
* **No.** The entire platform is open sourced. 
* **No.** The list of available facets and the functions that are included in them is freely available.

**Ok.. then how do you make money?**
* We have hosted the exact system that's freely available in this repo and added a super snazzy user interface to it. We charge a fee to use our interface.
* We have received grants to help us audit our contracts. 

**How do I know the contracts are secure?**
* Look at the metadata for each contract in the database. We add audit details and contract analytics in the contract metadata.

### Multi-Faceted Proxy Factory Contract Roadmap

- [x] Multi-Faceted Proxy Factor PRFAQ Live
- [ ] Multi-Faceted Proxy Wiki Live
- [x] Create initial codebase, and one sample 
- [ ] Create 50 sample Facets
- [ ] Build and Run tests for stored contracts
- [ ] Accumulate audited contracts (and functions) that are considered best practice for specific use cases and store. 
- [ ] Reconstruct the functions found in these contracts as EIP-2535 Diamond Facets and launch in testnet
- [ ] Build EIP-2535 Contracts that use these newly launched Facets.
- [ ] TODO

