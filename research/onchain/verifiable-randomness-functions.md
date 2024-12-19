---
description: Research notes for onchain Verifiable Randomness Functions (VRFs)
---

# Verifiable Randomness Functions

## Intro To VRFs

#### What is Verifiable Random Function (VRF) <a href="#what-is-verifiable-random-function-vrf" id="what-is-verifiable-random-function-vrf"></a>

A VRF or Verifiable Random Function is a unique blend of cryptographic techniques that generates pseudorandom numbers in a publicly verifiable manner. Think of VRF as a way to generate random numbers where:

* The entity possessing a secret key can compute the random number and also provide a proof of its correctness.
* Anyone with the public key can verify that the random number was indeed computed correctly, ensuring the integrity of the result.

In simple terms, VRFs are like cryptographic hash functions but with an added layer of public verification. They're an essential tool in systems where the trustworthiness of random outputs is highly important.

[YouTube - VRF Introduction](https://www.youtube.com/watch?v=2OzH8f3_Q9s)



{% content-ref url="vrf-gelato.md" %}
[vrf-gelato.md](vrf-gelato.md)
{% endcontent-ref %}

