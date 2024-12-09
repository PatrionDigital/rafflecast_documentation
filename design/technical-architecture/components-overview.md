# Components Overview

1. Warpcast Frontend (Frame):
   * User interface for entrants to interact with the raffles.
   * Accessible through the Warpcast app or web client.
2. Creator dApp:
   * Web interface for raffle operators to set up and manage raffles.
   * Integrated with Warpcast for publishing and managing channels.
3. Backend Services:
   * Offchain API: Handles operations such as logging user activity, managing offchain criteria, and distributing offchain prizes.
   * Onchain Contract: Smart contract deployed on the Base rollup (Ethereum Layer 2) to:
     * Enforce onchain raffle criteria.
     * Manage prize pools (fungible tokens or NFTs).
     * Implement (or integrate) verifiable random selection (VRF).
4. Database:
   * Stores offchain data, such as user participation, raffle criteria, and tracking entrant progress.
5. Blockchain Layer:
   * Smart contracts interacting with the Base rollup for:
   * Raffle creation and settlement.
   * Onchain prize distribution.
6. Warpcast Integration:
   * Provides APIs for channel sharing, account validation, and community joining incentives.
