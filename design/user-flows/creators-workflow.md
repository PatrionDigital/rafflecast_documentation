# Creator's Workflow

## Flow Diagram

```
graph TD;
    A[Creator Logs In] --> B[Create Raffle];
    B --> C[Define Raffle Criteria];
    C --> D[Set Closing Date];
    D --> E[Optional: Set Prize Distribution (Offchain/Onchain)];
    E --> F[Publish Raffle to Warpcast Channel];
    F --> G[Manage Raffles (by Channel)];
    G --> H[Track Entrants];
    H --> I[Automatically Reward Winner (Offchain/Onchain)];
```

## Flow Description

1. Raffle Creation\
   The creator accesses the Rafflecast dApp to create a new raffle. This involves:
   * Setting Criteria: The creator defines the rules for participation, including criteria such as owning specific tokens, following accounts, joining channels, or engaging with content.
   * Defining Rewards: The creator selects the rewards for the raffle, which could include fungible tokens, NFTs, or other digital assets. An option for onchain prizes (such as token or NFT airdrops) is available.
   * Setting a Closing Date: The creator specifies the closing date for the raffle, determining when the selection process will be finalized.
2. Publish and Share\
   Once the raffle is created, the creator publishes and shares it. This step includes:
   * Publishing to the Platform: The raffle is made available for entrants to see and participate.
   * Sharing on Social Media: The creator can share the raffle link on platforms such as X/Twitter, with the option to incentivize new users with extra entries if they create a new Warpcast account and join the creator’s community or channel.
   * Sharing to Warpcast: Creators can choose to share their raffle with a specific channel on Warpcast. This helps group and organize raffles by community and allows for exclusive raffles in premium channels.
3. Managing Raffles\
   Creators can manage and track the raffles they’ve set up. This includes:
   * Viewing Entrants: The creator can view the participants and their entry statuses, checking who has met the criteria.
   * Sorting and Grouping by Channel: Raffles can be grouped and sorted by the Warpcast channel they were shared to, helping creators manage raffles by community.
4. Raffle Settlement\
   Once the raffle is closed, the winner is automatically selected based on the onchain Verified Random Function (VRF). The creator is notified, and the raffle winner receives their rewards, which could be a fungible token, NFT, or any other digital or physical asset.
   * Onchain Prize Distribution: If the raffle includes onchain prizes, the winner is automatically rewarded with tokens or NFTs, directly delivered to their wallet.
   * Offchain Prize Distribution: If the raffle includes offchain prizes, the creator is responsible for manually distributing these prizes to the winner (e.g., sending gift cards, exclusive access, etc.).
