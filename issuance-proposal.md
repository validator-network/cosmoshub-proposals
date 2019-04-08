# Allow issuance of fungible tokens in the Cosmos Hub
### Cosmos network governance proposal
## Summary
Make it possible to issue custom tokens directly on the Cosmos Hub
## Overview
In its current state, the primary utility of the Cosmos hub are a working PoS model and governance mechanisms.

The utility of the hub is expected to improve when IBC, one of the biggest value propositions of the Cosmos network, is implemented and enabled.

The work on IBC is on-going at https://github.com/cosmos/ics and is on track to eventually become a standard for how to communicate between PoS blockchains.

In the meantime, the Cosmos Hub's singular utility will be transfer of its native fungible token ATOM and delegating to the impressive community of validators that have emerged.

This governance proposal is intended to gauge the interest of enabling issuance of fungible tokens directly in the Cosmos Hub, alongside its native ATOM token.

The advantages of implementing this proposal include
* Lowers the “barrier to entry” for organizations and entities wishing to leverage the existing security and community that has been established on Cosmos Hub. Not all projects may want or need to maintain their own zone.
* Attracts more value to the Cosmos Hub, thus increasing the value of the native ATOM token.
* Provides an immediate use for Cosmos Hub before the introduction of IBC.
The proposal restricts listing of new tokens to those that can pass the governance process, which can act as a quality filter for projects and increase the trust in the Cosmos Hub.

## Details
We propose that the governance proposal transactions are expanded with a new `ProposalKind`, e.g. `ProposalTypeAddToken`. This would allow new tokens to be introduced through standard governance without the need for network upgrades. The proposal should include an unlimited issuer address from where new tokens can be minted and destroyed.
# Implementation
The development effort should be undertaken by one of the entities in the following, prioritized list
* Tendermint, Inc.
* 3rd party development team under a grant from the Interchain foundation
* 3rd party development team financed by crowdfunding among the network participants

# Motivation
e-money.com has an immediate ambition to issue fungible tokens backed by fiat currencies in the Cosmos Network. The longer term goal is to launch a separate zone, but pending the arrival of IBC we expect that significant value can be created for the network by issuing directly on the Cosmos Hub.

Other projects will be able to use these tokens. Obvious use cases include services accepting fiat payments and wallet providers.

Validators and delegators will also benefit from the additional transaction volume on the network, which will lead to an increase in collected fees.

Full disclosure: e-money.com is part of the same group of companies as validator.network, the author of this proposal.
## Not in scope
 * _Token life cycle_ - The potential removal of an issued token from the Cosmos Hub is left for a future governance proposal, if deemed necessary.
## Voting options

|               |               |
| ---------------- |-------------|
| Yes              | I want the community to move forward with the idea of issuing custom tokens directly in the Cosmos hub. |
| No / NoWithVeto  | Custom tokens should only originate in other zones and be present in the Cosmos hub through IBC. |
