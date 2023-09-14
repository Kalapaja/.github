# [Kampela](https://kampe.la)

## Reasonably secure hardware wallet for the [Polkadot](https://polkadot.network) ecosystem

![kampela-logo-black-small](https://github.com/Kalapaja/.github/assets/152719/e2370cd8-d033-45e7-a971-6ada69aa6e81)

Kampela is a hardware implementation of [Polkadot Vault](https://signer.parity.io/) (previously known as Parity Signer).
It is a small card-shaped device (ideally comparable to a credit card form factor, to be carried in a wallet when needed) that accepts data through unidirectional NFC port and shows output on a monochrome electronic paper screen.
It has cryptographic strongbox with elliptic curves supported by Substrate — which only stores private keys (after initial import) and performs all signing operations on-chip.

Kampela is a natural (and long-discussed) extension of Parity Signer to leverage the most out of modern hardware-based crypto chips and drastically reduce Signer’s attack surface: no mobile OS, not extra platform features, no unexpected communication methods or airplane mode to take care of.

⚠️ Kampela is not a wallet! It is a signing tool, it is not able to track on-chain balances, validate things over chain-provided information or generate transactions on itself.

### Repo organization

This organisation has been created to split out the sub-project from the unwieldy [Alzymologist/kampela](https://github.com/Alzymologist/kampela) monorepo in September 2023.
If you're here following the link in that (now-archived) repo, the new project structure is the following:

| New repository | Original subfolder | Description |
|----------------|--------------------|-------------|
|[kampela-firmware](https://github.com/Kalapaja/kampela-firmware)|[`firmware/development`](https://github.com/Alzymologist/Kampela/tree/main/firmware/development)|Firmware sources and associated software projects|
|[kampela-hardware](https://github.com/Kalapaja/kampela-hardware)|['hardware/development'](https://github.com/Alzymologist/Kampela/tree/main/hardware/development)|Hardware design schematics and supplementary files|
|[kampela-common](https://github.com/Kalapaja/kampela-common)|['common'](https://github.com/Alzymologist/Kampela/tree/main/common)|Collection of shared libraries used by both "hot" and "cold" side of the project|
|[siltti](https://github.com/Kalapaja/siltti)|[application](https://github.com/Alzymologist/Kampela/tree/main/application)|Android companion app to interface with the device|
|[docs](https://github.com/Kalapaja/docs)|[docs/development](https://github.com/Alzymologist/Kampela/tree/main/docs/development)|Miscellaneous docs documenting different aspects of the project|

In addition to that, we're publishing both hardware and software sources of the [pilkki](https://github.com/Kalapaja/pilkki) project — the firmware flashing tool accompanying Kampela devkits.
