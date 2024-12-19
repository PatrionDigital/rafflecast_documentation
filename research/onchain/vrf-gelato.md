# VRF - Gelato

[Gelato Documentation - VRFs](https://docs.gelato.network/web3-services/vrf)

## General Notes

* Gelato VRF uses [Drand](vrf-drand.md), a decentralized randomness beacon
* High Level Flow:

```
 +------------------------+
 | 1. Contract Deployment |
 +------------------------+
          |
          v
 +-----------------------+
 | 2. Requesting         |
 |    Randomness         |
 +-----------------------+
          |
          v
 +-----------------------+
 | 3. Processing the     |
 |     randomness        |
 |       event           |
 +-----------------------+
          |
          v
 +-----------------------+
 | 4. Randomness Delivery|
 +-----------------------+
```

1. Gelato's implementation is localed here: [GelatoVRFConsumerBase.sol](https://github.com/gelatodigital/vrf-contracts/blob/main/contracts/GelatoVRFConsumerBase.sol)
2. . When a randomness request is made, `RequestedRandomness`event is emitted. The event contains two parameters:
   * `round` explicitly signifies which Drand round is targeted to fulfill the randomness,
   * `data` offers versatility for developers, it can be used to attach any supplementary information or context about the randomness request.
3. Listen for the emitted `RequestedRandomness` event and fetch the required random number from `Drand`.
4.  Internally, the system invokes the `fulfillRandomness` function in the requesting contract.

    **Callback Invocation and Data Decoding**

    The random number (sourced from `Drand`) is passed as the `randomness` parameter to the function. Additionally, the `data` parameter can carry any supplementary data provided during the original request or by the Gelato VRF.

* [Foundry Template](https://github.com/gelatodigital/vrf-nft) and [Quickstart](https://docs.gelato.network/web3-services/vrf/quick-start)
* Gelato VRF services necessitate that your Gelato balance is sufficiently funded. This balance caters to Gas fees and rewards Gelato Nodes for their computational tasks.\
  [1Balance Documentation](https://docs.gelato.network/web3-services/1balance)

## Security Considerations

* State Locking - After you initiate a request for randomness and before the random number gets delivered, it's essential to lock the relevant application state in your consumer contract. This step minimizes the risk of front-running attacks.
* Instead of using the received randomness directly, consider integrating it with our RNGLib. This approach:
  * Enables dynamic fetching of random values as required.
  * Offers protection against certain bet arbitrage attacks, especially when multiple applications operate simultaneously.
*

## Deficiencies/Risks

* Contrary to some other VRF providers, Gelato VRF is verifiable _**off-chain**_ but _**not on-chain**_. This is due to the nature of the BLS signatures used by Drand network, which are not yet supported at EVM level.&#x20;







