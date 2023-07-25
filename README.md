<div align="right">

  [![license](https://img.shields.io/github/license/block-foundation/blocktxt?color=green&label=license&style=flat-square)](LICENSE.md)
  [![website](https://img.shields.io/website?color=blue&down_color=red&down_message=offline&label=website&style=flat-square&up_color=green&up_message=online&url=https%3A%2F%2Fwww.blocktxt.org)](https://www.blocktxt.org)

</div>

---

<div>
    <img align="right" src="https://raw.githubusercontent.com/block-foundation/brand/master/src/logo/logo_gray.png" width="96" alt="Block Foundation Logo">
    <h1 align="left">block.txt</h1>
    <h3 align="left">A well-known .txt file for blockchain address identification</h3>
</div>

---

<p align="center">
    <img src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.svg" width="33%" alt="blocktxt Logo">
</p>

<div align="center">
  <a href="https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=bug_report.yml">Report a Bug</a>
  |
  <a href="https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Afeature-request%2CHelp+wanted+%F0%9F%AA%A7&template=feature_request.yml">Request a Feature</a>
  |
  <a href="https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Aquestion&template=question.yml">Ask a Question</a>
  |
  <a href="https://github.com/block-foundation/blocktxt/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Aenhancement&template=suggestion.yml">Make a Sugestion</a>
  |
  <a href="https://github.com/block-foundation/blocktxt/discussions">Start a Discussion</a>
</div>
<br/>


<details open="open">
<summary>Table of Contents</summary>

- [About](#about)
- [Quick Start](#quick-start)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

</details>

## Introduction

The block.txt project, initiated by the Block Foundation, presents a revolutionary and standardized approach to sharing blockchain-related information associated with a website. By providing a structured, machine-readable format, the project opens doors for numerous applications in the ever-growing blockchain ecosystem.

As blockchain technology permeates into various sectors, the need for a standardized way to identify and share blockchain addresses on websites has become increasingly apparent. Websites involved in blockchain activities such as accepting digital payments, donations, or operating smart contracts often need to publicly declare their blockchain addresses. The block.txt project answers this call by providing a YAML-based format that outlines crucial information about a site's blockchain activities, in a way that's both human and machine-friendly.

Whether you're a blockchain explorer trying to track down an address, a wallet software that needs to integrate a site's donation address, or a user curious about the blockchain activities of a site, block.txt aims to be the go-to solution. Furthermore, the project takes into consideration important aspects such as security, privacy, and standard web protocols to ensure a safe and seamless experience.

Backed by the reputable Block Foundation and maintained by a community of open-source contributors, block.txt promises to be a significant step towards a more interconnected and accessible blockchain web. We invite you to be a part of this exciting journey.


block.txt follows the [YAML](https://yaml.org/) syntax.

### Example

``` yml

---

# block.txt example

contact:

    name: Block Foundation
    website: https://www.blockfoundation.io
    email: info@blockfoundation.io

accounts:

    -
        name: Ethereum account
        description: Block Foundation Donation Account
        blockchain: ETH
        address: 

    -
        name: Bitcoin account
        description: Block Foundation Reserve Account
        blockchain: BTC
        address: 
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

### Logotype

| SVG   | Monochrome | Acccent |
| ----- | ---------- | ------- |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg)*`blocktxt-logotype-blue-white.svg`* | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.png" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.png)*`blocktxt-logotype-blue-white.png`* | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.webp" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.webp)*`blocktxt-logotype-blue-white.webp`* |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.svg" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg)*`blocktxt-logotype-gray-blue.svg`* | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.png" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.png)*`blocktxt-logotype-gray-blue.png`* |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.webp" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-gray-blue.webp)*`blocktxt-logotype-gray-blue.webp`* |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.svg" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg)*`blocktxt-logotype-transparant-blue.svg`* | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.png" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.png)*`blocktxt-logotype-transparant-blue.png`* |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.webp" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-blue.webp)*`blocktxt-logotype-transparant-blue.webp`* |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.svg" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg)*`blocktxt-logotype-transparant-gray.svg`* | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.png" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.png)*`blocktxt-logotype-transparant-gray.png`* |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.webp" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-gray.webp)*`blocktxt-logotype-transparant-gray.webp`* |
| [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.svg" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-blue-white.svg)*`blocktxt-logotype-transparant-white.svg`* | [<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.png" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.png)*`blocktxt-logotype-transparant-white.png`* |[<img align="center" src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.webp" width="100%">](https://github.com/block-foundation/blocktxt/master/res/logotype/blocktxt-logotype-transparant-white.webp)*`blocktxt-logotype-transparant-white.webp`* |

## Development

### Authors

**`block.txt`** is an open-source project by the **[Block Foundation](https://www.blockfoundation.io "Block Foundation website")**.

The Block Foundation mission is enabling architects to take back initiative and contribute in solving the mismatch in housing through blockchain technology. Therefore the Block Foundation seeks to unschackle the traditional constraints and construct middle ground between rent and the rigidity of traditional mortgages.

website: [www.blockfoundation.io](https://www.blockfoundation.io "Block Foundation website")

### Contributing

We'd love for you to contribute and to make **`block.txt`** even better than it is today!
Please refer to the [contribution guidelines](.github/CONTRIBUTING.md) for information.

## Legal Information

Please note that if you're implementing block.txt, it would be important to consider the security and privacy of the included addresses. In many cases, blockchain transactions are transparent and can be traced, so putting an address on a public website might expose information about the transactions and balances associated with that address.

### Copyright

Copyright &copy; 2023 [Block Foundation](https://www.blockfoundation.io/ "Block Foundation website"). All Rights Reserved.

### License

Except as otherwise noted, the content in this repository is licensed under the
[Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/), and
code samples are licensed under the [MIT License](https://opensource.org/license/mit/).

Also see [LICENSE](https://github.com/block-foundation/community/blob/master/LICENSE) and [LICENSE-CODE](https://github.com/block-foundation/community/blob/master/LICENSE-CODE).

### Disclaimer

**THIS SOFTWARE IS PROVIDED AS IS WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
