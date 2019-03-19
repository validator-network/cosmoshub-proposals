# Petition to the Interchain Foundation

This petition has been submitted on YYYY/MM/DD as proposal 1 on chain-id "cosmoshub-1".

** THIS PROPOSAL IS A DRAFT AND WORK IN PROGRESS. **

## Background

With the successful launch of Cosmos Hub, the community thanks the Tendermint team and Interchain Foundation for all its hard work to bring the network live.

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

While "extremely resilient" is subjective, the above distribution leaves room for improvement when contrasted to comparable networks such as IRISnet Hub.


## Purpose of this proposal

This proposal serves as a petition to the Interchain Foundation to delegate in such a manner, that network robustness is increased by flattening the voting power distribution.

We _suggest_ that a simple algorithm is devised and implemented in software, to assist the Interchain Foundation in the ongoing work of delegating. 

If this algorithm were implemented it software, the Interchain Foundation is encouraged to release it under an open source license to enable peer review and re-use.


## Example algorithm

While __it is not the intention of this proposal__ to provide a working and well tested algorithm, one is provided below here as way of example.

```
Select number of atoms to delegate, maximum of 100k atoms.
Set target validator = nil. # This is the validator that receives the delegation.
Set best distribution = nil. # This is the best (flattest*) distribution seen so far.

For each candidate validator in the validator set**
{
  Simulate delegation to validator.
  Calculate the simulated distribution based on above delegation.
  If the target validator is nil
  {
    Set target validator = candidate validator.
	Set best distribution = simulated distributed.
  }
  Else
  {
    If the simulated distributed is better (flatter) than the current best distribution
    {
      Set target validator = candidate validator.
      Set best distribution = simulated distributed.
    }
    Else if the distribution is equal to the current best distribution
    {
      If the commission of the target validator is greater than the candidate validator
      {
        Set target validator = candidate validator.
      }
    }
  }
}

* Flattened, i.e. the number of validators required to reach 33% has increased.
** For instance, this could be ALL validators, validators who passed basic security reviews 
and/or validators who missed less than X blocks the last month.
```



## Voting

Your vote on this proposal __only includes the petition__ for the Interchain Foundation to delegate in a manner that flattens voting power distribution.

This is not a vote on using an algorithm, nor a vote on the actual implementation such an algorithm if it were to be used.

Please vote accordingly:

| Vote       | Interpretation            |
| ---------- | ------------------------- |
| Yes        | I support this petition in the current form.  |
| No         | I do not support this petition in current form. |
| NoWithVeto | This matter should not be petitioned to the Interchain Foundation. |
