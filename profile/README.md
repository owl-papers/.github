<p align="center">
  <a href="" rel="noopener">
 <img src="https://bafybeigvaksubkpa3wvuvhah3zv64odjobx6aacya7cbarafyhc4f5hime.ipfs.dweb.link/owl_articles.png" alt="Project logo"></a>
</p>
<h3 align="center">Owl papers</h3>

<div align="center">

[![Hackathon](https://img.shields.io/badge/hackathon-chainlink-orange.svg)](https://chainlink-fall-hackathon-2021.devpost.com/)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE.md)

</div>

---

<p align="center"> Enabling decentralized peer reviews of academic research
    <br> 
</p>

## 📝 Table of Contents

- [Problem Statement](#problem_statement)
- [Idea / Solution](#idea)
- [Roadmap](#roadmap)

<!-- - [Dependencies / Limitations](#limitations)
- [Future Scope](#future_scope)
- [Setting up a local environment](#getting_started)
- [Usage](#usage)
- [Technology Stack](#tech_stack)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)
- [Acknowledgments](#acknowledgments) -->

## 🧐 Problem Statement <a name = "problem_statement"></a>

Peer review of academic papers is a process that depends largely on academic journals supervision. Also, the peer review process is most of the times unpaid, which doesn't give much incentive for researchers to actually do a lot of reviews. What if we could incentivize the peer reviews process economically using smart contracts? Not only that, but maybe also enable a marketplace for academic research where researchers could publish their papers and receive the full value of their study from readers, instead of receiving it from the intermediate of the academic journal? 

To understand our attempt to solve this problem, it is necessary to understand how the peer review process works right now. First, the author submits the manuscript. Then, it goes through a process to check if the paper is ready for publishing. After that, an editor validates if the research fits the journal and assures that it has good quality. It goes through some more validation, and it finally reaches the peer review stage. In a peer review, most of the times the author doesn't know who is reviewing their papers (single-blind review) or neither the review nor the author know each other (double-blind review). But this process can also be open, which means that both reviewers and the author could know each other.

One thing that would be really hard to achieve if this process runs entirely in smart contracts would be the trust that scientists have in science journals and it's reputation: doing all this review process in a decentralized network enables anyone to make reviews and low quality reviews, which means that it would consume a lot of time to find relevant reviews. So, in order for this to work in reality, it would be necessary some filter from journals on who can review, or at least some direction on which reviews are worth it. 

However, despite the problem of the "trust in journal authority" that was cited, there is still space for creating an economic incentive for reviews. 

<!-- 
- IDEAL: This section is used to describe the desired or “to be” state of the process or product. At large, this section
  should illustrate what the expected environment would look like once the solution is implemented.
- REALITY: This section is used to describe the current or “as is” state of the process or product.
- CONSEQUENCES: This section is used to describe the impacts on the business if the problem is not fixed or improved upon.
  This includes costs associated with loss of money, time, productivity, competitive advantage, and so forth. -->

<!-- Following this format will result in a workable document that can be used to understand the problem and elicit
requirements that will lead to a winning solution. -->

## 💡 Idea / Solution <a name = "idea"></a>

In order to incentivize peer review, we are going to view academic papers and it's reviews as NFTs. A smart contract is used to associate a paper manuscript with it's reviews. Using chainlink VRF, reviewers would be randomly chosen from an array of addresses, each one belonging to a reviewer.
Scientists would need to first subscribe to a smart contract as reviewers, to have a chance to review some papers. When reviewers are chosen, the review process would start and they would have some time to emit their review as an NFT and associate it to an academic research. Upon submitted review represented as an NFT, the reviewers can receive an reward in cryptocurrency, previously inserted into the smart contract.

Also, only authorized people should have access to the entire content of the paper. This will be done by sending a signed message to a back-end,
checking if the signer address contains the NFT and sending it fully if he does.

We also intend to create an NFT marketplace for selling articles. It's not the main idea of the project, but given that academic journals usually don't pay it fully to researchers what they earn from selling their research, researchers could have some interest in selling the result of their study in a decentralized marketplace, where the entire value someone bought it for goes to them. 

##  Roadmap for development  <a name = "roadmap"></a>


Steps before implementation:

- Understand an NFT and it's functions fully: https://www.youtube.com/watch?v=YPbgjPPC1d0;
- Understand how to use Chainlink VRF properly;
- Understand how to encrypt a message using public key of wallet in the backend;
- Understand how to implement metamask extension on the front-end and use it to buy and mint NFTs;
- Read the Moralis docs. We will use it to facilitate our development process;
 
Implementation steps: 
- Develop the ERC1155 that will represent papers as NFTs and enable minting of papers by researchers; [X]
- Implement a smart contract that will handle who will review and how long the process will be open;
- Create an NFT marketpĺace just for the sake of having a way to sell papers for public readers and proposing a decentralized way to pay researchers for their work;
- Deploy it all! (With all crypto related stuff on testnets)


<!-- ## ⛓️ Dependencies / Limitations <a name = "limitations"></a>

- What are the dependencies of your project?
- Describe each limitation in detailed but concise terms
- Explain why each limitation exists
- Provide the reasons why each limitation could not be overcome using the method(s) chosen to acquire.
- Assess the impact of each limitation in relation to the overall findings and conclusions of your project, and if
  appropriate, describe how these limitations could point to the need for further research.

## 🚀 Future Scope <a name = "future_scope"></a>

Write about what you could not develop during the course of the Hackathon; and about what your project can achieve
in the future.

## 🏁 Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development
and testing purposes. See [deployment](#deployment) for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them.

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running.

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

## 🎈 Usage <a name="usage"></a>

Add notes about how to use the system.

## ⛏️ Built With <a name = "tech_stack"></a>

- [MongoDB](https://www.mongodb.com/) - Database
- [Express](https://expressjs.com/) - Server Framework
- [VueJs](https://vuejs.org/) - Web Framework
- [NodeJs](https://nodejs.org/en/) - Server Environment

## ✍️ Authors <a name = "authors"></a>

- [@kylelobo](https://github.com/kylelobo) - Idea & Initial work

See also the list of [contributors](https://github.com/kylelobo/The-Documentation-Compendium/contributors)
who participated in this project.

## 🎉 Acknowledgments <a name = "acknowledgments"></a>

- Hat tip to anyone whose code was used
- Inspiration
- References -->
