# Interactions Overview

### For Entrants:

* Warpcast Frame handles:
  * Logging into Warpcast accounts.
  * Checking if users meet the raffle criteria (offchain & onchain).
  * Adding extra entries for new Warpcast users.
  * Backend interacts with Warpcast API to verify eligibility and logs participation.

### For Creators:

* Creator dApp facilitates:
  * Defining raffle parameters (criteria, closing date, prize distribution).
  * Publishing raffles to Warpcast channels.
  * Backend synchronizes onchain and offchain criteria with the database and smart contracts.

### For Selection and Prize Distribution:

* VRF on the Base rollup determines winners.
* Backend coordinates:
* Offchain prize distribution.
* Interaction with the blockchain for onchain rewards.
