# Exercise (Beginner) Move/Typescript

The below exercise aims to be used with new Solutions Engineers in order to get familiarised with Sui-specific Move and Typescript best practices. It will be delivered in a guided format, supported by a more experienced Solution Engineer.

## Prerequisites

1. Needs to have completed the basic Move training (including object management, dynamic fields)
2. Needs to have a solid understanding and/or have completed the [Udemy, TS course](https://www.udemy.com/course/typescript-for-professionals/learn/lecture/21434252#overview) and have read through the Typescript SUI SDK documentation  ([here](https://docs.sui.io/build/prog-trans-ts-sdk) and [here](https://github.com/MystenLabs/sui/tree/main/sdk/typescript)).
3. Get familiarised with coding standards:
    - https://docs.sui.io/devnet/build/dev_cheat_sheet
    - https://move-language.github.io/move/coding-conventions.html

## Requirements

Company CryptoPort wants to integrate with Sui. Their use case is the following:

- The main idea is an UBER on chain
- There are three actors Rider, Driver and the Admin
- The flow is as follows: A Rider is requesting a ride, a Driver accepts the ride and terminates it when they arrive at destination
- A Ride should at least contain the following fields:
    1. initial_distance (the estimated distance given by backend )
    2. actual_distance (the actual distance ridden)
    3. rider_id
    4. driver_id
    5. state (this can be pending, accepted, completed, cancelled)
- All Rides should be saved on chain
- A Ride can only be accepted by one Driver
- A Rider can only have one Ride that is pending or accepted
- A Rider with 10 completed rides will get a get free Ride ticket

**Note:** You will receive a set of Move tests that comply with the expected design of the exercise.
