# HIP 70: Boring Protocol

-   Author(s): [@FOMOBY](https://github.com/FOMOBY) [@franswan](https://github.com/franswan) [@vers_laLune](https://github.com/vers-laLune?tab=overview&from=2022-09-01&to=2022-09-22)
-   Start Date: 2022-07-31
-   Category: Economy
-   Original HIP PR:
-   Tracking Issue: TO DO
-   Status: In Discussion

## Summary

The objective of this proposal is to outline the creation of a dVPN SubDAO facilitated by Boring Protocol and Helium.

In response to [HIP-51](https://github.com/helium/HIP/blob/main/0051-helium-dao.md), this proposal outlines construction for the integration of Boring Protocol dVPN into Helium network as a subDAO with its own DNT (decentralized network token) known as BOP. With respect to the nature of difference between this potential subDAO and existing subDAOs, many of the guidelines provided in HIP-51 will need to be considered for new solutions.

## Motivation

The drivers for this proposal are as follows:

-   Privacy and Security for Helium “subscribers” and internet users as a whole
-   Security and Scalability of the L1 as proposed in HIP-51
-   Additional mechanisms for profitability to Helium Network infrastructure operators
-   Network growth to Boring Protocol to generate a viable and strong dVPN (more nodes = greater obfuscation opportunity)
-   Proving a model of multi chain redundancy to further secure network economics and participant profitability
-   Sustainability in manufacturing and distribution of hardware
-   Increased Utility and Security for EVM mechanisms like wHNT

## Background

For the Helium Network to grow globally in number of active devices and users, it is necessary to develop economic incentives and opportunities for the infrastructure operators participating in supporting the network. Adding utility and profitability to the hardware involved now and in the future will solidify the Helium network as a major player across many types of networks.

This proposal will require addition to the economic models set forth to further incentive individual participants' activity in new networks with the advantage of increasing profitability of said participants.

HIP 51 outlines basic requirements for existing models of the subDAOs within the Helium Network. For the purpose of this HIP, the integration of two networks would need to omit some aspects of the economic model to procure the privacy and security that operators seek within both ecosystems. However, the pursuit of bringing value to the Helium token model must remain present.

The opportunity to have HIP-51 subDAO layer 1 migrated to Solana is present in this proposal for the purpose of allowing the HNT/BOP mechanics to flourish as well as to capitalize on the potential for Helium with the Solana Mobile platform. While not necessary at this time, the eventual growth and overflow of Helium's “Network of Networks” could mean a more robust layer 1 is needed. The advantage of keeping Helium and Boring separate via Multi-chain interoperability is that node operators can still stand to profit in the event that one of the networks faces outage(s). Boring Protocol is privacy and security at its foundation, but can be grown to generate subDAOs of its own network models ie. Proxy networks, distributed storage etc.

Boring Protocol operates currently on the token model envisioned by its team and community and is discussed further in this proposal.

The technical and economic design decisions of the Helium Network today have been made around the flagship LoRaWAN Decentralized Network Protocol.

## Stakeholders

This proposal impacts all HNT holders and their ecosystem as well as all BOP holders and their ecosystem. The objective is to provide greater growth to both networks while equally providing opportunity to the economics of Helium hardware operators, simultaneously creating privacy access to Helium network infrastructure. The Helium token model is described in the HIP’s presented previous to this proposal. Borings tokenomics weigh several key factors to provide incentive for network growth and network strength.

The BOP token utility is mainly a settlement between “clients” of the dVPN and “operators” of nodes which are used to privately access the internet. Apart from this primary function the token is staked by node operators to present loyalty to the network and financial incentive to act in “good faith” as they operate exit nodes. As nodes remain connected they increase their opportunity for traffic/data to be directed through their node and increase their profitability as the token is settled on a data consumption rate.

It is possible that the multi-chain interoperability may include a portion of BOP to be vested into contract to create a wrapped BOP on the Helium chain as well as liquidity. This proposal could be beneficial in the event Solana incurs an outage(s) and would allow Boring to continue operation and settlement from Helium. Though this is not ideal, it may be a greater measure for stability of the dVPN itself and allow for this continued profitability to node operators within the existing Boring Network and the Helium Network.

In researching and writing this HIP, Boring has used our social forums to conduct numerous discussions within the Helium community to generate this proposal. Continued participation and discussion is greatly encouraged to ensure the proposal is in line with the needs of both communities.

## Detailed Description

An initial integration may not include all economic requirements as described in HIP51 as the model for such only sets forth guidance for network structures that previously existed within the Helium ecosystem. As Boring is an entirely separate access layer network, we propose that the Data Credit models proposed in other subDAOs be removed from the equation. As Boring grows and the opportunity to use DC as a solution within our network model presents itself the community can propose and implement such changes.

Boring Protocol will instead add utility and value to the Helium token ecosystem by allowing customers to pay using HNT. Therefore, we will allow a direct transaction of HNT to one of our wallets to fulfill the payment for the service, or we’ll have a smart contract on the Solana blockchain that allows an instant swap of HNT/USDC to pay for the requested service.

As Boring implements cross-chain bridges the potential for added user payment types increases as well as the ability to access clients who may use these other blockchain based tokens. The ability to onramp such users will strengthen the network in driving further revenues to the operators who services said clients.

We need to either use a smart contract for a DEX or CEX that allows the instant swap—therefore no liquidity pool of our side is needed, or we enable a direct HNT payment and we sell HNT/USDC at our back later.

Therefore, we will use the Helium payment system to purchase our given service of VPN.

Implementation of this proposal requires some key factors be settled beyond tokenomics. Distribution being the primary potential drawback. Boring Protocol and its existing economic model is primarily dependent on a strategic balance between number of consumers and online nodes servicing them. Technical boundaries of the hardware we have developed for (Rasp Pi4b) and the bandwidth node operators can distribute to users have resulted in a series of tests. These tests, while initial, have generated a balance of 10 simultaneous clients per node operated. While this balance is impossible to ensure given the decentralized nature of the protocol, it remains a good measure for the Boring Protocol model. Factors such as client needs in regional node selection, pricing of bandwidth and general quality of connection are to be considered.

It is important to fully understand the ways Boring Protocol node operators profit from the dVPN network to grasp the need to limit the number of total nodes on the network and how quickly the onboarding of dual mining HNT/BOP nodes should occur.

## Drawbacks

The implementation of this HIP would come with the changing of the subDAO structure and subsequently create precedent for other subDAOs to stray away from the initial model within HIP-51. Removing the Data Credits system from our implementation of Boring as a subDAO streamlines the user experience but also hinders the incentive structure the Data Credit system was designed to implement across multiple subDAOs. We believe that given BOP is already an SPL token, the Data Credit system is redundant in our implementation. However, in general this does create an avenue for future subDAO complication. 

Another drawback lies in the fact that not everyone who runs a Helium node currently will be able to run a Boring Node. As it stands there are limitations to the network and we dont want to overload the network by scaling too quickly. At first, we will only offer a few thousand nodes. Additionally, our current software creates a hardware limitation. Not every Helium node runs on Raspberry Pi 4 and consequently they cannot run Boring Protocol. Future iterations of Boring should be able to account for this, but as it stands this is a limitation. 

Lastly, as stated previously, BOP is a SPL token which means it operates on the Solana Network. Historically the Solana Network has had several network outages and Boring consequently inherents this drawback. These outages should become increasingly more rare or non-existent, but it is an inherent risk. 


## Rationale and Alternatives-

As it stands, the dVPN space has a very limited alternative models and none of which run on Solana (as is the case with [HIP 70](https://github.com/helium/HIP/blob/main/0070-scaling-helium.md)). The closest competitor [Orchid Protocol](https://www.orchid.com/), built on the Ethereum blockchain, is plagued by the network issues it inherits from its L1. This leads us to the goal of this proposal, to work out the best method of implementation with the Helium Foundation given the unique challenges posed by this project.

==_In addition to being the only Solana-native solution, we believe our implementation is in a position to define measures against spoofing. The Orchid Protocol has been associated with spoofing to hide latency issues. We are far enough along in our execution we can prove our dVPN implementation is resistant to spoofing._== 

If this HIP is not approved, there is a serious looming security risk for users on the network. While there may be users who are perfectly okay with there real-time location being exposed to all people on the network, the opportunity for nefarious actors to exploit this information goes without saying. As the MOBILE network is rolled out there will simply be far too great of a risk for users without this subDAO.


## Unresolved Questions

Prior to the merge of this HIP, we expect to have completely resolved economic questions regarding the best method for settlement. Currently, the alternatives are a DEX, CEX or a smart contract for easy HNT/USDC swaps. We also intend to make sure the economics of Boring are in-line with the values and goals of the Helium community. The economic incentives of Boring should benefit the community as well as reward early adopters.

Beyond the economic questions, we need to resolve strategic deployment of the network. We hope to determine who from the Helium team will work alongside us in order to properly incorporate Boring as a Helium subDAO. Additioanlly, we need to determine the way we will test Boring on the Helium network. The strategic implementation of these network tests would need to be simple and effective as to not disrupt the current users of both networks. 

On a technical level, countermeasures to prevent spoofing need to be finalized. We are far enough along in our architecture that we believe we can adequately prevent spoofing, but the final details need to be solidified.

The implementation of this HIP would add simplicity for the end-user experience. The data credit system which we are proposing is waived reduces redundancy for users of our network. Beyond pure simplicity, the additional security for users will be a vast improvement over its current state in the Helium Network. As stated previously, there is a looming threat to the safety of users due to the location assertion of Nodes. This risk will only continue to increase as the MOBILE Network is deployed as this location assertion will be in real time with virtually zero latency (as stated in[ HIP-53](https://github.com/helium/HIP/blob/main/0053-mobile-dao.md)).

Outside of the scope of this proposal, there is a dearth of properly implemented dVPNs. The current centralized model for dVPNs is quickly failing as the services exchange information on user traffic, fail to meet security standards (e.g. keeping users passwords in text files) and increasingly the cVPN IP addresses are being blacklisted. A functional dVPN in the marketplace would extend beyond the scope of the Helium Network and have far reaching positive consequences for privacy and security. 


## Deployment Impact

As it stands, the end-user faces a security risk due to location assertion. The hotspot from which a user telegraphs their location does so within a few hundred feet of their real-time location. This, especially as the MOBILE network continues its implementation, will pose a major real-time security risk for all users. The MOBILE network would telegraph real-time data of their exact location with zero latency. Boring Protocol acts as an obfuscation layer for the main Helium Network. 

Our proposal is to explore the best method for implementaion alongside the Helium Foundation. Given the novel nature of this subDAO, the impact of our deployment would be heavily determined by the process with which we move forward. Our current objective is to work side-by-side with the Helium foundation in order to implement Boring Protocol in a manner that is aligned with the goals of L1 Security and Scalability as proposed in HIP-51. The goal of this would be to properly build layers alongside the Helium Foundation so that our network can co-exist for 3G, 5G and LoRaWAN. 

This proposal would primarily impact HIP-51 as we are altering the implementation of the subDAO. We are proposing a multi-chain interoperable solution with settlements in HNT as opposed to using the current Data Credit system. Since we will not be broadcasting to the Helium Network, there is no need for a Data Credit. Additionally, BOP already acts with teh same functionality as a Data Credit eliminating the need. This change will simplify the process for the end-user as there will immediate settlement.  As previously stated we can either implement a DEX or CEX or run a smart contract with HNT/USDC settlement. This will also serve as on on-ramp for users to the Helium Network as there is a growing public need for a functional dVPN beyond the needs outlined in the scope of this proposal. 

This proposal would affect HIP-51 as it explicitly references the Data Credit system for subDAOs and we are proposing alterations to the subDAO implementation. Should HIP-70 pass there should be few continuity issues as Boring Protocol is currently on the Solana Network. However, should the proposal be rejected, a migration of Boring Protocol would be necessary. 

Our proposal is largely backwards compatible outside of the incongruency with HIP-51.


## Success Metrics

The success of the design can be determined simply by the number of active nodes within the Boring Protocol as well as the amount of bandwidth being traded for HNT. 

As stated earlier, our initial tests have generated a balance of 10 simultaneous clients per node operated. The number of nodes operated works as a good indication of total clients and the amount of bandwidth being trafficked on the subDAO serves to further solidify these estimates. The number of nodes operated additionally acts as a measure of network stability. More nodes provides more effective obfuscation. 

Discussions of complexity are almost tautologically multifaceted. For the same of simplicity we can discuss complexity as a measure of user friction and as a measure of technological misallocation of resources. The addition of nodes to the network while adding more complexity in a strict sense, allows for network redundancy and increased security. Additionally, the operation of Boring as a multinetwork interoperable subDAO allows for failsafe in the case of network outage(s). The increased complexity in this case allows for decreased end-user complexity. Additionally, off-chain metrics such as customer service tickets and sales metrics for our simpler improved hardware serves as a proxy for end-user complexity being appopriately managed. These off-chain metrics as well as active holders of BOP, smart contract interactions and increases in number of operational nodes will serve as a metric of user acceptance of this HIP. 

To prove performance increase, you would measure the bandwidth being utilized on Boring Protocol as well as the amount of nodes currently implemented. Each additional node $n$ in the graph adds ${(n-1)}$ options for a user's traffic to be redirected through. For bandwidth usage $B$, the increase in performance would be:

$B_{n}$ ${n}\choose{2}$ / $B_{(n-1)}$ ${(n-1)}\choose{2}$ 

This is the quotient of the bandwidth $B_{n}$ and  ${n}\choose{2}$ and the bandwidth $B_{(n-1)}$ and ${(n-1)}\choose{2}$ . Which simplifies to: 

${.5B_{n}}n{(n-1)} /{.5B_{n-1}}{(n-1)}{(n-2)}$  

=> $B_{n}n/B_{(n-1)}(n-2)$ 

This formula would represent the incremental improvement of an additional node added to the network and the additional bandwidth increase relative to the former node and bandwidth. 


## Platform Incentives

45% of the total supply of BOP has been set aside for a 10 year distribution to node operators based on key factors that will reward uptime, specific region and bandwidth availability for node operators. This will subsidize growth of the network in key regions that are desirable to VPN users. This distribution is outlined in the [Platform Incentives Documentation](https://file+.vscode-resource.vscode-cdn.net/Users/pro/Documents/Boring%20Protocol/HIP/0070-boring-protocol.md#link)

Early supporters operating V1 nodes are rewarded at 1.5X rates.

V2 operators are rewarded at 1.25x standard rates.

These nodes are authenticated through an NFT License they stake to their node.


## Bandwidth Exchange

All node operators who incur dVPN customer traffic are paid 95% of the proceeds from consumed data—measured in KB—as data is consumed on the network.

The remaining 5% flows back into the Boring treasury for future development and operational costs.

We have projected a single node with a standard internet connection of X can earn as much as $24-240 per month from this one earning method given consistent traffic and data consumption across their node. This projection is further detailed here: Basis & Core


## Subscriber Model

To further reach VPN users outside of the crypto economy, Boring will allow fiat payment from subscriber model users. A fixed monthly and discounted yearly rate will be applied to these types of users and 95% of the income from this earning method will be equally distributed to all node operators according to uptime and connection bandwidth during the given period. It is proposed that these earnings be distributed monthly or quarterly.

The remaining 5% of revenue will be directed into the Boring Protocol treasury for future development and operational costs.

By limiting the total number of nodes allowed on the network, Boring can ensure the existing operators remain profitable and servicing clients with quality connections. As the consumer demand grows, the ability to add nodes to the network will be both desirable to new participants and be able to be completed quickly as this balance is maintained.


## Future Integration

Other possible integrations we envision for 5G and WIFI clients on the Helium network is to have Boring dVPN as an optional product for their users to select and these nodes could offer this at a higher access cost than typical. We propose this be included in a future proposal to reduce the complexity of the current proposal and allow time to research and explore this topic.

Boring Protocol can later provide proxy network and data storage infrastructure within the Helium ecosystem and is currently exploring a path toward this.

With the potential for a Helium 5G network to service the Solana Mobile phone or SAGA platform, we also wish to explore a Helium SubDAO migration to Solana as a whole with this proposal providing some “first steps” in bringing Helium liquidity to the Solana chain.
