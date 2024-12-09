---
description: >-
  This page will give a high-level overview of the data models and APIs used in
  the project. Each page will contain detailed information that can serve as a
  technical reference.
---

# Data Models and APIs Overview



1. Data Models\
   The various data models used in the project, with specific attention to:
   * Raffle Model:
     * Raffle metadata (e.g., criteria, prizes, start/close dates, etc.)
     * Connections to entrants, creator, and the Warpcast channel where it’s shared
   * Entrant Model:
     * Information about the entrants, including criteria met, their account information, and entries into different raffles
   * Prize Model:
     * Structure for prizes, including both on-chain and off-chain prizes, and any information related to distribution
   * Transaction Model (if applicable):
     * Details about prize distributions, winner selection, and tracking
   * VRF Model (if applicable):
     * The VRF implementation for winner selection and how it’s integrated
2. APIs Overview\
   The API endpoints used by the system. Each section will describe what the endpoint does, the data it accepts, and the response it provides.&#x20;
   * Authentication APIs:
     * API for logging in with Warpcast accounts, verifying if users meet criteria, etc.
   * Raffle APIs:
     * Endpoints for creating, viewing, and updating raffles
     * Retrieving raffle information (e.g., criteria, entrants, prizes)
   * Entry APIs:
     * APIs for entrants to check eligibility, submit entries, and track participation
   * Prize Distribution APIs:
     * Endpoints to facilitate the transfer of prizes after the winner is selected
   * VRF Integration:
     * How the VRF API is integrated and used for random winner selection
3.  Data Flow and Integration

    Describes how the data models interact with each other through the APIs, with a focus on:

    * How a raffle entry flows from the frontend (e.g., the Warpcast frame) to the backend via APIs
    * The process of verifying eligibility based on defined criteria
    * How the VRF system integrates into the data flow to select winners
    * How prize distributions are triggered and tracked
    * Interaction with off-chain data, like the tracking of social media engagements (recasting/liking posts)
4.  Data Validation and Security

    Covers any validation rules and security measures in place to protect the data:

    * Validation of Criteria: Ensuring users meet the raffle criteria before entering
    * Secure Prize Distribution: How the prize distribution process ensures fairness and accuracy, especially for on-chain prizes
    * Authentication and Authorization: How the APIs ensure that only authorized users (entrants, creators) can perform certain actions
