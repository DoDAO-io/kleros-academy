## I'm an Arbitration Developer! 💻


## Introduction

Kleros is an open-source online dispute resolution protocol that uses blockchain, crowdsourcing, and game theoretical incentives to fairly adjudicate disputes.

To date, Kleros has been used to arbitrate insurance claims, curated registries, escrow payment disputes, oracle answers, and more.

This is done through an arbitration standard wherein disputes that occur in applications (the so-called 'Arbitrable' dApps in Kleros terminology) are sent to the Kleros Court. From here, jurors are drawn randomly and evidence is submitted to be assessed alongside the application's policy. Once the jury comes to a decision, the court sends a ruling message back to the application where the dispute originated.


    


---
## Evaluation





##### **Based on the intro, which of the following can be considered use cases for Kleros?**  
     
- [ ]  Minting NFTs
- [x]  Settling Payment Disputes
- [ ]  Yield Farming
- [x]  Token List Curation





##### **What is the role of Kleros Court according to the arbitration standard outlined above?**  
     
- [ ]  To write the policy for an application
- [ ]  To submit evidence for court cases
- [x]  To draw jurors and submit a ruling
- [ ]  A platform to buy and sell PNK tokens

    


---
## Request-Challenger Workflow

Arbitrable applications most often follow what's known as the Request-Challenge workflow; users  submit requests in a permissionless manner, which are '**optimistically**' accepted as valid/correct/justified after a certain amount of time has passed unless challenged. 

This workflow reduces the dependence on the participation of the parties involved for the correct execution of the agreement baked into the Arbitrable contract, as well as minimises the number of transactions needed to execute an agreement.

### Here are a few examples of how it works!

- **In Insurance** - Users of an insurance protocol can submit a claim request directly to the smart contracts managing the claim payouts. Claims are automatically deemed valid and consistent with the protocol's policy (and thus paid out), unless other users step in to challenge this submission by placing a deposit and providing evidence for ineligibility to the jury with reference to the relevant insurance policies. 

- **In Curation** - An entry submitted to a curated list automatically gets registered after a period of time, unless a user steps into challenge the entry, providing arguments/evidence showing non-compliance with the listing criteria of the list.

- **In Escrow Payments** - A freelancer submits work to a client and is able to claim payment from the escrow if nobody (in this case probably the client) does not dispute the payment within a certain amount of time. To create a dispute, the user escalates the case to Kleros Court, citing why the work of the freelancer has not fulfilled the terms of the trade as established at the start of the contract.

    


---
## Evaluation





##### **Which of the following workflows complies with the Request-Challenge model?**  
     
- [ ]  Users deposit stablecoins into a protocol and are rewarded with an interest bearing token.
- [ ]  Users provide liquidity to a token pool in exchange for a portion of the trading fees in this pool.
- [x]  A user submits their profile to a Sybil-resistant registry of humans. Another user sees that the submission does not comply with the policy of the registry and challenges the entry.
- [ ]  An artist auctions their piece at a given floor price and the buyer who places the highest bid by the end of the auction period receives the artwork.
- [ ]  Funds locked in a escrow contract always requires active action from the payer to release the funds to the payee.

    


---
## Technical Interfacing

## Arbitrable vs Arbitrator

![How Kleros Works](https://3482524208-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LPbPWuMtwBOvW0iuxyw%2Fuploads%2Fgit-blob-8d377e7918f3509618161378338a8cfeacfcf2b7%2Faa1%20(2).jpg?alt=media)

As stated in the ERC-792 arbitration standard, arbitrable applications must define the actions to be taken when a ruling is received from the arbitrator. To do this, the arbitrable side must implement the logic for the `rule` function and emit a `Ruling` event. It is also the responsibility of the arbitrable application to call the `createDispute` function from the arbitrator's interface.

Functions for the creation of disputes and appeals are defined in the arbitrator interface, as well as the corresponding view functions required to compute appeal cost and appeal period. Additional view functions defined in this interface are also responsible for returning the status of a dispute and the current ruling. When the jury comes to a decision, the arbitrator calls the `rule` function defined in the arbitrable interface.

## Evidence vs MetaEvidence

![ERC-1497](https://3482524208-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LPbPWuMtwBOvW0iuxyw%2Fuploads%2Fgit-blob-6ad9498efd07d5375b73728d30f2fde5419aa893%2Fimage%20(7)%20(2)%20(2)%20(2)%20(2)%20(2)%20(2).png?alt=media)

The ERC-1497 evidence standard is rather simple, consisting of a single interface housing three events - `MetaEvidence`, `Evidence`, and `Dispute`.  MetaEvidence pertains to the information about a dispute; the agreement, parties involved, what needs to be decided, ruling options, and so on. While Evidence is a piece of information to support a proposition on either side of an argument. The Dispute event present in the interface emits the arbitrator of the contract, the ID of the dispute, the ID of the MetaEvidence for the dispute, and the ID for the evidence group linked to the dispute.

    


---
## ERC-792 and ERC-1497

## Technical Details

### Helpful Links:
- [Arbitrable Interface](https://github.com/kleros/erc-792/blob/master/contracts/IArbitrable.sol)
- [Arbitrator Interface](https://github.com/kleros/erc-792/blob/master/contracts/IArbitrator.sol)
- [Evidence Interface](https://github.com/kleros/erc-792/blob/master/contracts/erc-1497/IEvidence.sol)

### ERC-792 Functions:
- `rule()`
- `createDispute()`
- `appeal()`
- `arbitrationCost()`
- `appealCost()`
- `appealPeriod()`
- `disputeStatus()`
- `currentRuling()`

### ERC-792 Events:
- DisputeCreation
- AppealPossible
- AppealDecision
- Ruling

### ERC-1497 Events:
- Evidence
- MetaEvidence
- Dispute

    


---
## Long Quiz

You’ve made it to the home stretch! Here’s one last test to tie everything together, starting with a few easy questions to warm up and ramping up in difficulty as you go along.




##### **1. Which statement best describes Kleros?**  
     
- [ ]  A marketplace for hiring lawyers fluent in blockchain technology.
- [ ]  An automated market maker
- [x]  A decentralised dispute resolution protocol
- [ ]  A platform for buying and selling NFTs





##### **2. Who is responsible for adjudicating disputes sent to the Kleros Court?**  
     
- [ ]  A group of DAOs pre-selected by the Kleros Cooperative.
- [ ]  A single entity granted judicial power through Kleros governance.
- [ ]  Members of a nation state where the dispute originated from.
- [x]  A crowdsourced jury drawn at random.





##### **3. Which function belongs to the Arbitrable Interface?**  
     
- [ ]  appealCost()
- [ ]  createDispute()
- [ ]  disputeStatus()
- [x]  rule()





##### **4. Which event belongs to the Arbitrator Interface?**  
     
- [ ]  Dispute
- [ ]  Ruling
- [x]  AppealPossible
- [ ]  Evidence





##### **5. Which statement most acurately describes the difference between Evidence and MetaEvidence?**  
     
- [ ]  MetaEvidence is the policy of a decentralised application while Evidence contains information about a dispute.
- [ ]  MetaEvidence contains information about the evidence group and arbitrator of a dispute while Evidence is the policy of a decentralised application.
- [x]  Evidence are pieces of information that support propositions to either side of a dispute, while MetaEvidence contains all the relevant information about the dispute itself including parties involved and ruling options.
- [ ]  None of the above.





##### **6. The Arbitrator interface defines the event to be emitted when a ruling is given. True or false?**  
     
- [ ]  True
- [x]  False





##### **7. The Arbitrable interface defines the view function for returning the status of a dispute. True or false?**  
     
- [x]  False
- [ ]  True





##### **8. The Arbitrable interface defines the function to create disputes while the Arbitrator interface defines the function to take a ruling. True or false?**  
     
- [ ]  True
- [x]  False

    


---
## 🎉🎉🎉

Congratulations, you made it to the end of this guide! Whenever you’re ready to take the next step in bringing justice to the decentralised world, head over to our [Integration Guide](https://kleros.gitbook.io/docs/integrations/overview) for an in-depth look at how to build and ship your first arbitrable dApp. 

- [Link to Full ERC-792 Documentation](https://developer.kleros.io/en/latest/index.html)
- [Link to Full ERC-1497 Documentation](https://developer.kleros.io/en/latest/erc-1497.html)

    

