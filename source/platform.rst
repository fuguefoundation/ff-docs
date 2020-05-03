.. _ref-platform:

########
Platform
########

****************
Project Overview
****************
.. index:: ! Decentralized Application
.. index:: ! Ethereum
.. index:: ! Application Programming Interface
.. index:: ! Non-fungible Token
.. index:: ! Effective Altruism

The Fugue Foundation manages a few open source projects, which combine together to create an Ethereum-based donation platform guided by the principles of effective altruism.

.. image:: _static/ff-dapp-flow.jpg

When a user visits the decentralized application (dApp), the dApp queries a dataset of nonprofit organizations through an application programming interface (API) and populates four options. These options are charity evaluators (Give Well, 80,000 Hours, The Life You Can Save, and Animal Charity Evaluators), each based around a different issue (global poverty and well-being, helping women and girls, global health and COVID-19, and helping animals, see :ref:`ref-partnership`). 

Each grouping is a collection of nonprofit organizations identified by the charity evaluator for their track record of altruistic impact within the given area of concern. The user selects one of these evaluators, sees the corresponding nonprofits, and is given the option to research them further or proceed to the donation page. Think of each donation as a contribution to a charitable index fund. All donations are in ``ether`` (ETH), though we plan to incorporate ERC20 tokens soon such as DAI and USDC. Through the logic encoded in the smart contracts deployed the Ethereum blockchain, the donation is split evenly among the chosen nonprofits and the user is rewarded with a non-fungible token (NFT).

****
dApp
****

* Angular 9
* Truffle
* Open Zeppelin
* Solidity

The angular frontend and the smart contract backend are being developed separately for now. However, the angular dapp does have services providing a functional Truffle/Web3 integration, which will make combining the two later very simple.

For the frontend, the focus is on improving functionality, improving UX/UI (Angular Material), and writing tests (Karma, Jasmine, Protractor). The prototype is based off of the Angular `Tour of Heroes tutorial <https://angular.io/tutorial>`_ and the Web3 integration is based off a `Truffle Angular box <https://github.com/Quintor/angular-truffle-box>`_.

For the smart contract backend, it is `Truffle <https://www.trufflesuite.com/docs/truffle/overview>`_ compilation with modified `Open Zeppelin <https://docs.openzeppelin.com/contracts/2.x/>`_ contracts. Specifically, there is an ``ERC721`` contract and a ``PaymentSplitter`` contract that should work together, meaning that once a user makes a donation of a certain value, s/he will receive a unique edition of the Fugue Foundation NFT. `Block Native <"https://www.blocknative.com/>`_ is also integrated to help make the ``web3`` experience as user friendly as possible. The focus currently is to build out a few of the methods to each contract to capture this functionality, and to write tests (in both Solidity and Javascript) to capture the intended behavior.

* *Angular Frontend*: https://github.com/fuguefoundation/ff-dapp 
* *Smart Contract Backend*: https://github.com/fuguefoundation/ff-contracts

***
API
***

* MongoDB
* Node.js
* Javascript 

The RESTful API is meant to not only serve as the data source for the dapp, but also to grow as a resource for the entire effective altruism community. Over the coming months, we hope to get insight from charity evaluation experts on the best metrics and data structures to use in order to model the API into something that academics, altruists, journalist, data scientists, and others will want to use in their own projects.

The API currently runs on Heroku in a dev environment. There are two primary objects - ``nonprofits`` and ``evaluators`` - each exposed through ``GET``, ``POST``, ``PATCH``, and ``DELETE`` requests. In the short term, the goal is to build out the API in a secure and efficient fashion. However, long term the key is to create datasets that make other organizations want to use this resource to further their own research goals.

* *API repo*: https://github.com/fuguefoundation/ff-api
* See :ref:`ref-api`


