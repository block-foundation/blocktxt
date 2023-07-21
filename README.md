<div align="right">

  [![license](https://img.shields.io/github/license/block-foundation/blocktxt?color=green&label=license&style=flat-square)](LICENSE.md)
  [![website](https://img.shields.io/website?color=blue&down_color=red&down_message=offline&label=website&style=flat-square&up_color=green&up_message=online&url=https%3A%2F%2Fwww.blocktxt.org)](https://www.blocktxt.org)

</div>

---

<div>
    <img align="right" src="https://raw.githubusercontent.com/block-foundation/brand/master/logo/logo_gray.png" width="96" alt="Block Foundation Logo">
    <h1 align="left">block.txt</h1>
    <h3 align="left">A well-known .txt file for blockchain address identification</h3>
</div>

---

<p align="center">
    <img src="https://raw.githubusercontent.com/block-foundation/blocktxt/master/res/logo.svg" width="25%" alt="blocktxt Logo">
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

<br/>
<details open="open">
<summary>Table of Contents</summary>

- [About](#about)
- [Quick Start](#quick-start)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

</details>

## About

`block.txt` provides data about the blockchain activities associated with a website. This includes addresses for receiving payments or donations, smart contract addresses related to the site's services, or addresses related to any other blockchain activities.

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

|   |   |   |   |
|---|---|---|---|
|   |   |   |   |

## Development

### Authors

**`block.txt`** is an open-source project by the **[Block Foundation](https://www.blockfoundation.io "Block Foundation website")**.

The Block Foundation mission is enabling architects to take back initiative and contribute in solving the mismatch in housing through blockchain technology. Therefore the Block Foundation seeks to unschackle the traditional constraints and construct middle ground between rent and the rigidity of traditional mortgages.

website: [www.blockfoundation.io](https://www.blockfoundation.io "Block Foundation website")

### Contributing

We'd love for you to contribute and to make **`block.txt`** even better than it is today!
Please refer to the [contribution guidelines](.github/CONTRIBUTING.md) for information.

## Legal

Please note that if you're implementing block.txt, it would be important to consider the security and privacy of the included addresses. In many cases, blockchain transactions are transparent and can be traced, so putting an address on a public website might expose information about the transactions and balances associated with that address.

### License

Except where otherwise noted, **`block.txt`** by Geoid is licensed under the terms of the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/ "Creative Commons Attribution-ShareAlike 4.0 International License"). To view a copy of this license, visit [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/ "Creative Commons Attribution-ShareAlike 4.0 International License") or write to Creative Commons, 171 Second Street, Suite 300, San Francisco, CA 94105, USA.

### Disclaimer

**THIS SOFTWARE IS PROVIDED AS IS WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
