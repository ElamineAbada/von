---
permalink: /about/
title: "About Verifiable Organizations Network (VON)"
excerpt: "About Verifiable Organizations Network - what we've started and where we're going"
last_modified_at: 2019-01-21T12:00:00-07:00
toc: true
toc_sticky: true
---
# Quick Start: Webinars

> To see and hear about what we are building, [watch this webinar](https://bc-von.s3.amazonaws.com/2018-06-VON-Webinar-for-Sovrin-Indy-Community.mp4) by John Jordan of the BC Government about OrgBook and the Verifiable Organizations Network (VON).

# Background - Adding Trust to the Internet

The goal with the VON project is to enable organizations&mdash;and the people running those organizations&mdash;to conduct business online in a trusted manner. The core challenge is that on the Internet we can't tell if we're talking to you, or someone pretending to be you. We need a reliable way to verify that "you are you" in a manner appropriate for the type of transaction that you want to complete and in a privacy-preserving manner. The imposter problem is made worse by the rise in cyberattacks that expose user's personal data that might otherwise be useful in proving identity. With all of the data about you in the wild, we need new approaches to verifying that you have the authority to conduct an online transaction.

Putting Internet users&mdash;and organizations&mdash;in control of their own online identity has been a growing need since the start of the Internet. With the creation of massive centralized stores of private data (e.g. Equifax, Google, Facebook, etc.), has grown the ability for holders of that data to use (and misuse) that data in ways that are not always in the best interest of the data owner, you. As we move forward with identity, we also want to put you in control of where and how your data is used.

The goals of trusted identity and control over your own data has created an urgency to change how our data&mdash;data we (should) own&mdash;is handled. [Self-sovereign identity](https://bitsonblocks.net/2017/05/17/a-gentle-introduction-to-self-sovereign-identity/) (SSI) is a promising approach to decentralize the handling of personal data that gives users back control of their data, where it belongs. SSI further enables a higher level of trust on the Internet by providing mechanisms that enable verifiable identification of parties to a transaction, reducing the need for high-cost, in person mechanisms to establish trust. With SSI, people can't pretend to be you simply by showing they know things about you (your name, address, user id, password, etc.).

The VON project is particularly focused on bootstrapping the trust attribute of the SSI approach for organizational entities. We aim to create a trusted digital network of verifiable data about organizations, which is globally connected, interoperable, secure, and easy to join. We believe the novel capabilities of distributed ledger based, self-sovereign identity ecosystems to provide increased levels of trust for online transactions will foster economic activity for BC companies locally and across the globe.

## The First Step - Creating a Network Effect

We recognize there is an immediate chicken-and-egg challenge in creating VON&mdash;a network of [verifiable credential](https://w3c.github.io/vc-data-model/) issuers/verifiers (services, such as government issuers of permits and licences) and holders (organization clients for those services). The challenge is a lack of services issuing verifiable credentials about organizations, and a lack of organizations with the ability to hold verifiable credentials about themselves.

To bootstrap VON we are using strategies suggested in this excellent [presentation](https://a16z.com/2016/03/07/all-about-network-effects/) by the venture capital firm [Andreessen Horowitz](https://a16z.com) on building network effects. A network effect is needed when a product or service becomes more valuable to its users only when there enough people they know using it. This effect has been observed in any successful communications network from the telephones to Facebook.

The particular strategy we are putting into action is similar to the one that was deployed by Facebook. [TheFaceBook](http://www.thecrimson.com/article/2004/2/9/hundreds-register-for-new-facebook-website/) at Harvard used a clever network effect to bootstrap the new world of Social Networks. Mark Zuckerberg pre-loaded [TheFacebook (circa 2004)](https://web.archive.org/web/20040212031928/http://thefacebook.com) with accounts that provided a core of users sharing a single common attribute&mdash;they went to Harvard. This one step triggered a network effect, magnifying the subsequent actions of users and resulting in the ever-faster growth of TheFaceBook's, and ultimately, Facebook's, social network. Without seeding the network, that growth may not have come.

We're trying to use VON's ["OrgBook"](https://orgbook.gov.bc.ca) (formerly called "TheOrgBook") to generate that same network effect for building organizational self-sovereign identities and the use of [verifiable credentials](https://w3c.github.io/webpayments-ig/VCTF/charter/faq.html).

## Triggering Network Effects for VON

The challenge in creating an organizational SSI network is:

* **Supply:** Services don't supply verifiable credentials because there are no organizations with their own SSI digital wallet.
* **Demand:** Organizations don't have their own SSI digital wallets because there are no services that supply verifiable credentials.

The BC Government can't directly influence the demand side or provide tools, such as digital wallets, for organizations. That's for commercial providers to support. However, as a major supplier of credentials (registrations, licenses, permits, etc.) to organizations, BC can enhance its government services to drive the supply side&mdash;and indirectly, demand. OrgBook gives government services a place to issue public verifiable credentials and from which to receive proofs of verifiable claims&mdash;without requiring organizations to have their own agents and wallets.

Here's a simple picture of the system:

<figure>
  <img src="{{ '/assets/images/issuing-credentials-with-orgbook.png' | relative_url }}" alt="Issuing and Verifying Credentials with OrgBook">
</figure>

* On the right are government services that organizations access to apply for a variety of credentials, including registrations, permits and licenses.
  * The services use instances of [VON issuer/verifier agents](https://github.com/bcgov/von-agent-template) to verify claims and issue credentials.
  * Services could cross governmental jurisdictions (provincial, regional, municipal) and could even involve commercial entities (banks, etc.).
* In the middle, (The)OrgBook is a repository of public credentials issued by those services to OrgBook.
  * Credentials are equivalent to the "Permit to Operate" documents posted on businesses' walls.
  * (The)OrgBook's repository of public credentials is web-searchable, listing organizations, credentials and credential details (claims).
* On the left is a representative of an organization that is applying for registrations, licences and permits from the services on the right.
* The identity registry (represented by the file folders with links) underlies the system to infuse trust.
  * The identity register is a decentralized, self-sovereign identity network built on blockchain/distributed ledger technology.
  * The initial VON implementation uses the [Sovrin Foundation](https://sovrin.org)'s Sovrin Network as the underlying Identity Registry Network.

As an organization goes through the online application processes to acquire registrations, licenses or permits, the services get proofs (and their associated verified claims) from verifiable credentials already stored in OrgBook about the organization. Once a service completes the approval process and decides to issue the organization a registration, licence or permit, they issue that public verifiable credential digitally to OrgBook about the organization.

* This saves the users from having to re-type the information for each service (and eliminates typos in the data).
* Each service can trust the information because it comes from a trusted source, cryptographically proving:
  * The information was issued by the issuer
  * The information was issued to OrgBook
  * The information has not been tampered with (was not forged)
  * The information has not been revoked

## The Code

All of the VON code is open source and found on [GitHub](https://github.com/topics/verifiable-organizations-network). To learn more about the VON components, check out this [VON overview]({{ "/getting_started/von-overview/" | relative_url }}).

## Want to know more?

To learn more about VON, move on to our [get started](/getting_started/get-started) page for more about the business and technical elements of VON with lots of links about what we are building.

## Want to help?

Fork the code, [connect with us](mailto:swcurran@cloudcompass.ca,john.jordan@gov.bc.ca?subject=Contributing to VON) and let's build VON together.