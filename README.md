




# Secondbitcoin

[![Website](https://img.shields.io/badge/Website-secondbitcoin.com-blue)](http://secondbitcoin.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub Issues](https://img.shields.io/github/issues/secondbitcoin/secondbitcoin)](https://github.com/secondbitcoin/secondbitcoin/issues)

http://secondbitcoin.com

## What is Secondbitcoin?

Secondbitcoin is an independent blockchain network that forked from Bitcoin's genesis block, creating a separate chain. The project uses modified software based on the original Bitcoin Core codebase.

This project serves as a testing ground for blockchain technology exploration and cryptocurrency development, providing developers and researchers with an environment to experiment with Bitcoin-based protocols without affecting the main Bitcoin network.

## Features

- **Genesis Fork**: Built from Bitcoin's original genesis block
- **Dual Version Support**: Compatible with both legacy (v0.12.1) and modern (v29.0) implementations
- **Mining Enabled**: Built-in mining capabilities for network participation (v0.12.1 only)
- **Full Node Support**: Complete blockchain node implementation

## Getting Started

### Prerequisites

Before you begin, ensure you have the following:

- **Operating System**: 
  - Ubuntu 16.04 LTS (for v0.12.1-second)
  - Ubuntu 24.04 LTS (for v29.0-second)
- **Build Tools**: Standard C++ development environment
- **Git**: For repository management

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/secondbitcoin/secondbitcoin.git
cd secondbitcoin
```

#### 2. Select Your Version

Choose the appropriate branch based on your Ubuntu version:

**For Ubuntu 16.04 LTS:**
```bash
git checkout v0.12.1-second
```

**For Ubuntu 24.04 LTS:**
```bash
git checkout v29.0-second
```

#### 3. Build the Project

Follow the [Bitcoin Core build documentation](https://github.com/bitcoin/bitcoin/blob/master/doc/build-unix.md) for detailed compilation instructions. 


> **Note**: Specific build dependencies and configuration options may vary between versions. Refer to the `doc/` directory in your chosen branch for version-specific instructions.

### Configuration

#### Mining Setup (v0.12.1-second)

To enable mining on the v0.12.1-second branch, add the following configuration to your `bitcoin.conf` file:

```ini
gen=1
```

The configuration file is typically located at:
- **Linux**: `~/.bitcoin/bitcoin.conf`
- **Create the file if it doesn't exist**




## Contributing

We welcome contributions to the Secondbitcoin project! 


## Documentation

- [Project Wiki](https://github.com/secondbitcoin/secondbitcoin/wiki)

## Support

### Getting Help

- **Wiki**: Explore our comprehensive [project wiki](https://github.com/secondbitcoin/secondbitcoin/wiki)
- **Issues**: Report bugs or request features via [GitHub Issues](https://github.com/secondbitcoin/secondbitcoin/issues)
- **Email**: Contact the development team at [cubist.signer_7f@icloud.com](mailto:cubist.signer_7f@icloud.com)

### Community

- **Discussions**: Join [project discussions](https://github.com/secondbitcoin/secondbitcoin/discussions) in the GitHub repository
- **Website**: Visit [secondbitcoin.com](http://secondbitcoin.com) for updates and announcements

## License

This project is licensed under the MIT License.

## Acknowledgments

- **Bitcoin Core**: This project is built upon the foundational work of the Bitcoin Core development team
- **Open Source Community**: Thanks to all contributors who make blockchain development possible


## ⚠️ Important Disclaimer

**CRITICAL WARNING**: 

- **This is NOT Bitcoin**: Secondbitcoin is a completely separate blockchain network and is NOT the official Bitcoin (BTC)
- **Do NOT transfer BTC**: Never send Bitcoin (BTC) to Secondbitcoin addresses - your funds will be **permanently lost**
- **Do NOT transfer to BTC**: Never attempt to send Secondbitcoin coins to Bitcoin addresses - your funds will be **permanently lost**
- **Different Networks**: These are entirely separate blockchain networks with no interoperability

**Additional Warnings**:
- This is experimental software provided for educational and research purposes only
- Use at your own risk - no warranties or guarantees are provided
- Do not use this software in production environments without thorough testing


**By using this software, you acknowledge that you understand these risks and accept full responsibility for any losses that may occur.**


**Below is the original README file from Bitcoin Core, preserved for reference.**


Bitcoin Core integration/staging tree
=====================================

https://bitcoincore.org

For an immediately usable, binary version of the Bitcoin Core software, see
https://bitcoincore.org/en/download/.

What is Bitcoin Core?
---------------------

Bitcoin Core connects to the Bitcoin peer-to-peer network to download and fully
validate blocks and transactions. It also includes a wallet and graphical user
interface, which can be optionally built.

Further information about Bitcoin Core is available in the [doc folder](/doc).

License
-------

Bitcoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/license/MIT.

Development Process
-------------------

The `master` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly from release branches to indicate new official, stable release versions of Bitcoin Core.

The https://github.com/bitcoin-core/gui repository is used exclusively for the
development of the GUI. Its master branch is identical in all monotree
repositories. Release branches and tags do not exist, so please do not fork
that repository unless it is for development reasons.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled during the generation of the build system) with: `ctest`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python.
These tests can be run (if the [test dependencies](/test) are installed) with: `build/test/functional/test_runner.py`
(assuming `build` is your build directory).

The CI (Continuous Integration) systems make sure that every pull request is tested on Windows, Linux, and macOS.
The CI must pass on all commits before merge to avoid unrelated CI failures on new pull requests.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://explore.transifex.com/bitcoin/bitcoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.
