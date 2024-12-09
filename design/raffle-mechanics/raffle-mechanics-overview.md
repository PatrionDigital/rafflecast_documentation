# Raffle Mechanics Overview

The Raffle Mechanics section will define how raffles are structured and function within the system. It will cover the following key areas:

1. [Raffle Creation](raffle-creation.md)
   * Creator’s Role: Raffle creators will be responsible for setting up the raffle. This includes defining the raffle criteria, selecting a closing date, setting up the prize distribution (both on-chain and off-chain), and choosing the Warpcast channel for sharing.
   * Criteria: Creators can set criteria for entry, such as holding specific tokens or NFTs, following specific accounts, liking/recasting content, etc. These criteria will be used to verify eligibility.
2. [Entrant Participation](entrant-participation.md)
   * Entry Process: Entrants must meet the defined criteria in order to participate in the raffle. Once eligibility is verified, they can enter the raffle.
   * Account Requirements: Entrants must log in with their Warpcast (Farcast) account and may need to create one if they don’t have one. Additionally, any required criteria must be met before they can officially enter.
3. [Prize Distribution](prize-distribution.md)
   * Prize Setup: Prizes can be distributed either off-chain (e.g., physical items, discount codes, etc.) or on-chain (e.g., tokens, NFTs, etc.). Creators can select one or both options for the raffle.
   * Rewarding Winners: After the raffle closes, a winner is selected, and the prize(s) are automatically distributed. This includes both on-chain and off-chain rewards, as configured by the creator.
4. Raffle Settlement and Winner Selection
   * Closing: The raffle automatically closes at the designated time. If there are multiple eligible entrants, a winner is selected.
   * Selection Mechanism: A Verifiable Random Function (VRF) will be used to ensure a fair and transparent selection of winners. This mechanism will be either implemented directly or integrated from a third-party service.
   * Prize Distribution: After winner selection, prizes are distributed based on the configured prize distribution method.
5. [Raffle Management and Tracking](raffle-management-and-tracking.md)
   * Creator Dashboard: Creators can track entrants and manage their raffles via a dedicated dashboard. This includes monitoring entrants, reviewing raffle progress, and managing criteria or raffle settings.
   * Post-Raffle Actions: Creators and entrants can review the winner’s details and ensure the prize distribution happens smoothly. If applicable, creators can also trigger additional actions like notifications or exclusive offers for entrants.

The Raffle Mechanics section will ensure that raffles run efficiently, ensuring fairness for all participants while providing an easy-to-use interface for creators to manage and distribute their raffles. This section will also be tightly integrated with Warpcast for entry and community building.
