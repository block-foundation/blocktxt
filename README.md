<div align="right">

[![GitHub License](https://img.shields.io/github/license/block-foundation/blocktxt?style=flat-square&logo=readthedocs&logoColor=FFFFFF&label=&labelColor=%23041B26&color=%23041B26&link=LICENSE)](https://github.com/block-foundation/blocktxt/blob/main/LICENSE)
[![devContainer](https://img.shields.io/badge/Container-Remote?style=flat-square&logo=visualstudiocode&logoColor=%23FFFFFF&label=Remote&labelColor=%23041B26&color=%23041B26)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/block-foundation/blocktxt)

</div>

---

<div>
    <img align="right" src="https://raw.githubusercontent.com/block-foundation/brand/master/src/logo/logo_gray.png" width="96" alt="Block Foundation Logo">
    <h1 align="left">block.txt</h1>
    <h3 align="left">A well-known .txt file for blockchain address identification</h3>
</div>

---

<img align="right" width="75%" src="https://raw.githubusercontent.com/block-foundation/brand/master/src/image/repository_cover/block_foundation-structure-03-accent.jpg"  alt="Block Foundation Brand">

### Contents

- [Introduction](#introduction)
- [Quick Start](#quick-start)
- [Colophon](#colophon)

<br clear="both"/>

---

<div align="right">

[![Report a Bug](https://img.shields.io/badge/Report%20a%20Bug-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=bug_report.yml)
[![Request a Feature](https://img.shields.io/badge/Request%20a%20Feature-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=feature_request.yml)
[![Ask a Question](https://img.shields.io/badge/Ask%20a%20Question-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=question.yml)
[![Make a Suggestion](https://img.shields.io/badge/Make%20a%20Suggestion-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=suggestion.yml)
[![Start a Discussion](https://img.shields.io/badge/Start%20a%20Discussion-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=discussion.yml)

</div>

## Introduction

The `block.txt` project, initiated by the Block Foundation, presents a revolutionary and standardized approach to sharing blockchain-related information associated with a website. By providing a structured, machine-readable format, the project opens doors for numerous applications in the ever-growing blockchain ecosystem.

As blockchain technology permeates into various sectors, the need for a standardized way to identify and share blockchain addresses on websites has become increasingly apparent. Websites involved in blockchain activities such as accepting digital payments, donations, or operating smart contracts often need to publicly declare their blockchain addresses. The block.txt project answers this call by providing a YAML-based format that outlines crucial information about a site's blockchain activities, in a way that's both human and machine-friendly.

Whether you're a blockchain explorer trying to track down an address, a wallet software that needs to integrate a site's donation address, or a user curious about the blockchain activities of a site, block.txt aims to be the go-to solution. Furthermore, the project takes into consideration important aspects such as security, privacy, and standard web protocols to ensure a safe and seamless experience.

Backed by the reputable Block Foundation and maintained by a community of open-source contributors, block.txt promises to be a significant step towards a more interconnected and accessible blockchain web. We invite you to be a part of this exciting journey.

block.txt follows the [YAML](https://yaml.org/) syntax.

### Example

``` yml

---

# block.txt

contact:
    name: Your Organization Name
    website: https://yourwebsite.com
    email: contact@yourwebsite.com
    socials: 
        twitter: yourTwitterHandle
        linkedin: yourLinkedInProfile
        github: yourGithubProfile

additionalContacts:
    - 
        name: Additional Contact Name
        role: Role in the organization
        email: additionalcontact@yourwebsite.com
        phone: +1-234-567-8901

emergencyContacts:
    - 
        name: Emergency Contact Name
        email: emergencycontact@yourwebsite.com
        phone: +1-123-456-7890

accounts:
    -
        name: Main Ethereum account
        description: Main Account for Ethereum Transactions
        blockchain: ETH
        network: Mainnet
        address: 0xYourEthereumAddress
        verification: https://link-to-proof-of-ownership
        tags:
          - donations
          - main
        operators: 
          - Operator Name
        purpose: Accepting Donations
        created: YYYY-MM-DD
        active: true
        multisig: false
        security: Medium
        extraNotes: Extra information about the account
        archived: false

    -
        name: Bitcoin Donation account
        description: Bitcoin Donation Account
        blockchain: BTC
        network: Mainnet
        address: YourBitcoinAddress
        verification: https://link-to-proof-of-ownership
        tags:
          - bitcoin
          - donations
        operators: 
          - Operator Name
        purpose: Bitcoin Donations
        created: YYYY-MM-DD
        active: true
        multisig: false
        security: High
        extraNotes: Extra information about the account
        archived: false

    -
        name: Other Blockchain account
        description: Description for this account
        blockchain: Blockchain Name
        network: Your Blockchain Network
        address: YourAddressOnThisBlockchain
        verification: https://link-to-proof-of-ownership
        tags:
          - otherBlockchainName
          - payments
        operators: 
          - Operator Name
        purpose: Payments
        created: YYYY-MM-DD
        active: false
        multisig: true
        security: Low
        extraNotes: Extra information about the account
        archived: true

additionalInformation:
    organizationProfile: https://link-to-organization-profile
    projectOverview: https://link-to-project-overview

updated: YYYY-MM-DD  # replace with last updated date in ISO 8601 format

```

## Quick Start

### 1. Create

#### 1.1 Filename

Create a text file called **`block.txt`**.
Always use lower-case formatting for the filename.

#### 1.2 Encoding

Make sure that the **`block.txt`** file is UTF-8 encoded to avoid issues with special characters and multiple languages.

### 2. Place

#### 2.1. well-known Directory

In principle, the **`block.txt`** file should be placed under the `/.well-known/` path of your website [[rfc8615](https://datatracker.ietf.org/doc/html/rfc8615)]. For example:

``` bash
https://example.com/.well-known/block.txt
```

#### 2.2. Root Directory

If the `/.well-known/` directory cannot be used for technical reasons, or if you want to use a fallback option, the **`block.txt`** file can also be placed in the `root` directory of your website. For example:

``` bash
https://example.com/block.txt
```

The **`block.txt`** file can be placed in both locations of a website at the same time. Hence, the final directory structure for your website could look like this:

``` bash
example.com/
├── index.html
├── block.txt
└── .well-known
    └── block.txt
```

### 3. Link

#### 3.1. Head

Place a reference to the file using a `“help”` tag to the `<head>` section of your website. For example:

``` html
<link type="text/plain" rel="help" href="https://example.com/block.txt"/>
```

#### 3.2. Button

Embed a **`block.txt`** button to your site and link it to your **`block.txt`** file.

### 4. Serve

#### 4.1. Internet Media Type

The **`block.txt`** file should have an Internet Media Type of `text/plain`.

#### 4.2. Protocol

The **`block.txt`** file must be served over HTTPS.

## Logo

You can download the official **`block.txt`** logos and include them in your own online projects.
We encourage placing the logo in the footer, and don’t forget to add a link to your **`block.txt`** file!

> For example:

``` html
<a href="/well-known/block.txt"><img src="/assets/image/blocktxt_logo.png"></a>
```

For the full list of of official **`block.txt`** logos, see the table below:

### Logomark

| SVG           | PNG           | WEBP          |
| ------------- | ------------- | ------------- |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-blue-white.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-blue-white.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-blue-white.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-blue-white.png) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-blue-white.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-blue-white.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-gray-blue.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-gray-blue.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-gray-blue.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-gray-blue.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-gray-blue.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-gray-blue.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-blue.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-blue.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-blue.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-blue.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-blue.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-blue.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-white.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-white.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-white.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-white.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-white.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-white.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-gray.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-gray.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-gray.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-gray.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-gray.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-transparant-gray.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-blue.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-blue.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-blue.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-blue.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-blue.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-blue.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-gray.svg" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-gray.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-gray.png" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-gray.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-gray.webp" width="100">](https://github.com/block-foundation/blocktxt/master/res/logomark/blocktxt-logomark-white-gray.webp) |

### Logotype

| SVG           | PNG           | WEBP          |
| ------------- | ------------- | ------------- |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.png) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-blue.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-blue.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-blue.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-blue.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-blue.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-blue.webp) |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-gray.svg" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-gray.svg) | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-gray.png" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-gray.png) |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-gray.webp" width="200">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-white-gray.webp) |

---

## Colophon

### Authors

This is an open-source project by the **[Block Foundation](https://www.blockfoundation.io "Block Foundation website")**.

The Block Foundation mission is enabling architects to take back initiative and contribute in solving the mismatch in housing through blockchain technology. Therefore the Block Foundation seeks to unschackle the traditional constraints and construct middle ground between rent and the rigidity of traditional mortgages.

website: [www.blockfoundation.io](https://www.blockfoundation.io "Block Foundation website")

### Development Resources

#### Contributing

We'd love for you to contribute and to make this project even better than it is today!
Please refer to the [contribution guidelines](.github/CONTRIBUTING.md) for information.

### Legal Information

#### Copyright

Copyright &copy; 2023 [Stichting Block Foundation](https://www.blockfoundation.io/ "Block Foundation website"). All Rights Reserved.

#### License

Except as otherwise noted, the content in this repository is licensed under the
[Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/), and
code samples are licensed under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).

Also see [LICENSE](https://github.com/block-foundation/community/blob/master/src/LICENSE) and [LICENSE-CODE](https://github.com/block-foundation/community/blob/master/src/LICENSE-CODE).

#### Disclaimer

**THIS SOFTWARE IS PROVIDED AS IS WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
