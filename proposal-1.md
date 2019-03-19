# Petition to the Interchain Foundation

This petition has been submitted on YYYY/MM/DD as proposal 1 on chain-id "cosmoshub-1".

** THIS PROPOSAL IS A DRAFT AND WORK IN PROGRESS. **

## Background

With the successful launch of Cosmos Hub, the community thank the Tendermint team and Interchain Foundation for all its hard work to bring the network live.

The community is now looking forward for the network to stabilize and the enabling of transfers to drive user adoption.

As of 2019/03/19 the top 5 validators, ranked by voting power, are:

| Validator      | Voting Power |
| -------------- | ------------ |
| Certus One     | 10.29%       |
| Polychain Labs | 10.16%       |
| stake.fish     | 10.09%       |
| Dokia Capital  | 9.37%        |
| Figment        | 8.22%        |


Without consideration to the historical performance and good intentions of these validators, we find it concerning to see a concentration of voting power considering the 33% threshold for liveness.

For users, integrators and developers to trust the Hub with their business, it must be understood to be extremely resilient in a wide range of failure modes.

While "extremely resilient" is subject, the above distribution leaves room for improvement when contrasted to comparable networks such as IRISnet Hub.


## Purpose of this proposal

This proposal serves as a petition to the Interchain Foundation to delegate in such a manner, that network robustness is increased by flattening the voting power distribution.

We suggest that a simple algorithm is devised and implemented in software, to assist the Interchain Foundation in the ongoing work of delegating. 

This software should be released under an open source license to enable peer review and re-use.


## Example algorithm

While it is not the intention of this proposal to provide a working and well tested algorithm, one is provided here as way of example.

```
Select number of atoms to delegate, maximum of 100k atoms.
Set target validator = nil.

For each candidate validator in the validator set*
{
  Simulate delegation to validator
  If the distribution has flattened (i.e. the number of validators required to reach 33% has increased)
  {
    If the target validator is nil
    {
      Set target validator = candidate validator.
    }
    otherwise, if the commission of the target validator is above the candidate validator
    {
      Set target validator = candidate validator.
    }
  }
}

* For instance, this could be ALL validators, validators who passed basic security reviews 
and/or validators who missed less than X blocks the last month.
```



## Voting

Your vote on this proposal __only includes the petition__ for the Interchain Foundation to devise and use an algorithm to flatten voting power distribution.

The actual *implementation* of the algorithm is outside the scope of this proposal.

Please place your accordingly:

| Vote       | Interpretation            |
| ---------- | ------------------------- |
| Yes        | I support this petition.  |
| No         | I do not support this petition in current form. |
| NoWithVeto | I do not support petition the Interchain Foundation. |
