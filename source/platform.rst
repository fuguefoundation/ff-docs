.. _ref-platform:

########
Platform
########

*The Fugue Foundation dApp and API are under development*

Visit our homepage at `fuguefoundation.org <https://fuguefoundation.org>`_ or our `Github repos <https://github.com/fuguefoundation>`_ for more information.

****************
Project Overview
****************
.. index:: ! Decentralized Application
.. index:: ! Ethereum
.. index:: ! Application Programming Interface
.. index:: ! Non-fungible Token
.. index:: ! Effective Altruism

The Fugue Foundation manages a few open source projects, which combine together to create an Ethereum-based donation platform guided by the principles of effective altruism.

Insert diagram flow

When a user visits the decentralized application (dApp), the page queries a dataset of nonprofit organizations through an application programming interface (API) and populates four selections. These are three groupings (plus one create-your-own option) of nonprofits based on the criteria of certain charity evaluator organizations such as Give Well, Charity Navigator, and Effective Altruism (see :ref:`ref-partnership`). The user then selects one of these options and sends ether or any ERC20 token to the dApp. Through the logic encoded in the Fugue Foundation smart contracts deployed the Ethereum blockchain, the donation is split among the chosen nonprofits and the user is rewarded with a non-fungible token (NFT). 

****
dApp
****

* Angular 9
* Truffle
* Open Zeppelin

***
API
***

* MongoDB
* Node.js
* Express
