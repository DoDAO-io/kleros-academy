## Juror Onboarding Guide (en)


## The role of jurors in Kleros

As you might already have learnt in our [community onboarding guide](https://kleros.dodao.io/onboarding/guide/view/60f7555c-30aa-48be-8dac-915b3cbea53b/4), Kleros is a decentralized dispute resolution service that relies on a jury to perform arbitration on all kinds of disputes in a trustless and decentralized manner.

While jury systems exist in real-world jurisdictions like the United States, Canada and Ireland, **[Kleros](https://kleros.io)** is the first and only functioning jury-based dispute resolution system in Web3. It has several features that makes it uniquely effective and suitable for truly decentralized applications:
* **Random selection** - jurors are randomly drawn using a provably random number generator, minimizing collusion between disputants and jurors.
* **Juror anonymity** - jurors are free to conceal their real identities behind their on-chain addresses, preventing blackmail and collusion.
* **Governance by economic incentives** - coherent voters in a case are rewarded economically, while incoherent voters have their stakes 'slashed' (partially taken away), creating an incentive for jurors to vote carefully.
* **Self-selection of jurors** - access to the jury is permissionless, and the penalties of voting incoherently deter jurors from self-selecting themselves into courts which they lack the knowledge to arbitrate on.
* **Appeal system** - The ability for anyone on the internet to appeal a case and challenge the judgment of the jury in a case drastically increases the security of the court against random voting, bribes and collusion.

    


---
## Getting started as a juror

Taking part as a juror is easy - simply buy some **Pinakion/PNK** tokens, go to the [Kleros Court interface](https://court.kleros.io) and stake in the court that you feel most comfortable with contributing as a juror.

![Diagram showing steps to becoming a juror](https://blog.kleros.io/content/images/2020/09/Jurors-start.png "3 steps to becoming a juror")

Here are the links to bring you directly to where you need to be:

1. Download a wallet (we recommend [Metamask](https://metamask.io/))
2. Buy some Pinakion/PNK tokens (see list of decentralised and centralised exchanges [here](https://kleros.gitbook.io/docs/pnk-token))
3. The [Court interface ](https://court.kleros.io/) (available on the Ethereum and Gnosis chain)
4. Overview of the [available courts in Kleros](https://kleros.gitbook.io/docs/products/court)

    


---
## Processes of Kleros Court

All disputes initiated in Kleros go through these 5 stages:

1. **Evidence** - Evidence can be submitted. This is also when drawing of jurors takes place.
2. **Commit** - Jurors commit a hashed vote. This is skipped for courts without hidden votes. 
3. **Vote** - Jurors reveal/cast their vote depending on whether the court has hidden votes or not. 
4. **Appeal** -  The dispute can be appealed. 
5. **Execution** - Tokens are redistributed and the ruling is executed.

The overall flow is visualized in this diagram:
![Diagram showing the processes in Kleros Court](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LPbPWuMtwBOvW0iuxyw%2Fuploads%2FanPuZOrP5JrAUT0KHt1k%2Fimage.png?alt=media&token=67762a69-d1f1-46fd-8c36-6c05fa54afc7 "Kleros court processes visualised")


    


---
## Evaluation #1

Great! 

Now let's test your knowledge of the things discussed so far!




##### Which of the following options describe how you get selected to be part of the jury of a dispute?  
     
- [x]  I need to have acquired some PNK tokens and staked them in the Kleros Court in question.
- [ ]  I need to have submitted my educational qualifications for verification.
- [ ]  I need to be whitelisted by the disputants and/or Kleros.
- [x]  I need to have been drawn as a juror by the randomized drawing process.
- [ ]  The dispute needs to take place during my birthday month.
- [ ]  I cannot be part of the organisation that is involved in the disputes.

    


---
## Reviewing the 'Primary Document'

The most important document present in every dispute is the **primary document**, which is a (PDF) file that describes the terms and conditions of the agreement that precedes the dispute, and lays out the rules for its resolution. Its role is similar to that of a piece of law or contract used for resolving real-world disputes, and forms the basis for jurors to decide what is the right ruling.

In the diagram below, you can see a link to the primary document at the bottom of the screen in the Kleros Court interface: 
![Screenshot showing the primary document displayed at the bottom of the voting interface](https://i.imgur.com/ClqvF9m.jpeg "Primary document link at the bottom of the Court interface")

Here are a couple of links to primary documents used in past disputes:
- [Unslashed Finance](https://ipfs.kleros.io/ipfs/QmeTBY7jZe2ut5WjifNASADo3E4zBxkMd62WwBpXtwP9pg)
- [Kleros Tokens](https://ipfs.kleros.io/ipfs/QmTL1SCKpRcr7NRbVpXW6z9QoQXRHJT5cQr6PEge5qoLwU/t2cr-primary-document.pdf)
- [Proof-of-Humanity](https://ipfs.kleros.io/ipfs/QmXDiiBAizCPoLqHvcfTzuMT7uvFEe1j3s4TgoWWd4k5np/proof-of-humanity-registry-policy-v1.3.pdf)

    


---
## Reviewing evidences

Evidences are documents uploaded in support of a particular outcome to a case. These can be anything from plain text, images to extensive (PDF) documents with in-depth analysis and argumentation.

In the Kleros evidence standard (aka [ERC-1497](https://kleros.gitbook.io/docs/developer/erc-1497-evidence-standard) for the technically inclined), evidences are managed by the '*Arbitrable*' application (see the [ERC-792 Arbitration standard](https://kleros.gitbook.io/docs/developer/erc-792-arbitration-standard)), which is the application responsible for creating the dispute in Kleros Court and enforcing the ruling that comes back from it. They are then displayed in Kleros Court, and meant to be interpreted by the jurors using the Primary Document as backdrop.

![Relationship between Arbitrables and Arbitrators](https://3482524208-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LPbPWuMtwBOvW0iuxyw%2Fuploads%2Fgit-blob-8d377e7918f3509618161378338a8cfeacfcf2b7%2Faa1%20(2).jpg?alt=media)

**Provenance of evidences**

It is important to note that there can be people outside of the disputants and the jury that would like to submit evidences or arguments (e.g. experts, impassioned community members, people with access to special information/knowledge). Therefore, most Arbitrable applications actually allow anyone on the internet to submit evidences as long as they are willing to expend gas to upload the evidence. 

While each piece of evidence should be reviewed on its own merits, it can be insightful to know what the possible sources of evidences are in a case, and which categories of evidence (submitters) are or are not represented.

    


---
## Voting coherently

In the Kleros system, a vote is **coherent** if it coincides with the majority choice, and is rewarded with a coherence reward at the conclusion of a case. On the other hand, incoherent votes will lead to the voter's stake getting slashed and redistributed to the coherent voters. It is also important to know that you must vote if you are drawn; otherwise you get slashed by default. 

Coherence is only determined at the end of an entire dispute. If a vote was coherent only in the first round of a dispute, the voter could still be slashed at the end of a dispute if the final round of appeals led to a different ruling.

**Refusing to arbitrate**

There is always the option to choose to '**Refuse to arbitrate**' in any dispute on Kleros Court. 
This option is reserved for situations where it is not reasonable for the jury to rule, which includes but are not limited to the following:
* The case involves a topic that is inconsistent with the Court's policy (e.g. asking to rule on topics involving assassination markets, porn)
* The jury is unable to access or verify the information presented in the case to make an informed vote.
* The case was wrongly assigned to the court in question (e.g. a translation dispute case being brought to a technical blockchain court)

Voting to 'Refuse to arbitrate' is considered as valid a choice as any other options presented to the jurors. You will therefore not be slashed for inactivity, and will be given coherence rewards if the majority chooses to 'Refuse to arbitrate' too, and slashed if you are in the minority.




    


---
## Appealing rulings

As shown in the diagrams in the section about the processes in Kleros Court, every round of voting is followed by an appeal stage. When a case is in appeal, anyone can appeal the case by placing the deposit, which will escalate the case into another round of arbitration with a larger and different set of jurors.

The opportunity to appeal is especially interesting for jurors whose choice ended up being the minority choice of a round; if you believe you are truly right, you can appeal the case and upload new evidences and arguments to convince the next round of jurors. This gives you a chance to vindicate yourself and stand a chance to win a higher reward (e.g. coherence reward plus the deposit & stakes of those who supported the opposing side).

    


---
## Evaluation #2





##### Which of the following are possible outcomes for a juror after a case concludes?  
     
- [ ]  I can do nothing in a case I'm drawn into (e.g. not vote at all) and face no consequences.
- [ ]  If I voted 'incoherently' (e.g. in the minority) after the voting phase of a round has concluded (but appeal phase still ongoing), I would have already been slashed.
- [x]  If I voted 'coherently' (e.g. in the majority) after the final voting and appeal phase of a case have concluded, I will be safe from slashing and eligible for a coherence reward.
- [x]  Voting 'Refuse to arbitrate' is considered 'voting' and I will not be slashed for inaction.
- [x]  As a coherent voter, I will be eligible for a reward in ETH (on Ethereum), and potentially an additional portion in PNK from the slashed stakes of incoherent voters.





##### Which of the following are true regarding the appeal mechanism of Kleros Court?  
     
- [ ]  Only the jurors in the current round can appeal a case.
- [ ]  When a case is appealed, the same jurors from the previous round are drawn in to vote again.
- [x]  If an appeal is started and only one side funds the appeal, that side automatically wins the dispute regardless of the ruling in the last round.
- [x]  An appeal can be crowdfunded, with potential winnings from the dispute distributed to the.crowd funders proportionally to the size of their contributions.





##### Which of these are good reasons to base your vote on?  
     
- [x]  Ignoring the merits of a case if the subject matter already violates the rules of the court in question.
- [ ]  Going to social media to find other jurors, and base your vote on the most popular opinion of the crowd.
- [ ]  Basing your vote on a published bribe by one of the disputants.
- [x]  Voting to reject a 'reasonable' claim because it failed to follow procedures laid out in the policy/primary document.
- [x]  Basing your vote on balanced discussions about the merits of a case in a Kleros community chat.

    


---
## Hurray, you are done!

Congrats on making it to the end of this juror onboarding guide! 

For a detailed step-by-step guide on how to go through the staking and voting process, check out this [guide here](https://kleros.gitbook.io/docs/products/court/kleros-juror-tutorial).

Once you feel confident enough it's time to contribute to decentralized justice with your newfound knowledge as a juror in [Kleros Court](https://court.kleros.io)!

    

