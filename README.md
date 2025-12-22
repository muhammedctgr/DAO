# DAO

## Decentralized Autonomous Organization

It's not entirely accurate, but an easy way to think about a DAO is like a big company where all the actions of the company are decided upon by Immutable, Transparent, Decentralized voting mechanisms.

This affords the users of a system the power to control and direct how it evolves over time, instead of leaving this power in the hands of centralized control, behind closed doors.

Decentralized voting/governance is the cornerstone of how these systems operate!

## DAO Architecture

Let's look a little closer at the properties of a DAO that allow them to function.

Voting Mechanism

This is the means by which a community engages with the protocol and contributes to the decisions being made. This is a fundamental part of how a DAO functions.

One consideration that must be made is: How do we identify stakeholders, or members of the community, eligible to vote?

Often this is handled via an ERC20 or an NFT of some kind, but this runs the risk of being less fair if the tokens are more available to the wealthy than others. This is not dissimilar to Web2 companies and how the voting power of company shares works.

One methodology is the "Skin in the Game" method whereby voting records are recording and negative outcomes result in tokens/voting power being lost. This is beneficial in that it holds users accountable for the decisions they make. A downside to this approach is how difficult it can be to reach a consensus on what a bad outcome is.

A third approach is something called "Proof of Personhood Participation" and while potentially ideal, isn't something with a sound implementation yet. The idea would be a method by which someone can be verified as being a single human entity, but the logics of this are difficult and rub up against anonymity. Some projects like WorldCoin are trying to find solutions here!

Voting Implementation

On-chain Voting:

Handled via smart contract, votes are placed by calling functions to this contract. A major drawback of this is the gas costs associated with placing this vote transaction. Even small costs in gas can be enough to dissuade participation, and that's to say nothing of transactions which happen to be expensive due to congestion or poor code.

Off-chain Voting:

What if I told you, you could sign a transaction and vote in a decentralized way without spending any gas?

Transactions can actually be signed without being sent to the blockchain. What this means is a protocol could take a bunch of signed transactions, uploaded to a decentralized database (like IPFS), calculate the votes and then batch submit them to the blockchain, maybe even leveraging an oracle to ensure decentrality. This can reduce voting costs by up to 99%!

It's important to be careful the the implementation of any off-chain features, if you introduce a centralized component, the decentrality of your DECENTRALIZED autonomous organization goes away.

## Tools

There are a number of no-code/low-code tools that can facilitate a DAO, services like DAO Stack, Aragon, Colony and DAO House can greatly assist in the operations side of running a DAO.

Additional tools with more granular control and integrations include things like Snapshot which allows a team to glean sentiment of a community before execution while also including functionality to manage and execute proposals if desired. Other tools to check out include Zodiac a development library offered by Gnosis and our old friends OpenZeppelin. We'll be using the OZ library in our development for sure!

Lastly, another "tool" I want to mention is Safe (previously Gnosis Safe), or really any multisig wallet solution. Any protocol is going to have some degree of centrality, especially as it first launches. A multisig wallet will decentralize control to some degree while a protocol grows into adopting fully decentralized governance.

## In this Project

1. We are going to have a contract controlled by a DAO
2. Every transaction that the DAO wants to send has to be voted on
3. We will use ERC20 tokens for voting 