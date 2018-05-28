# blockchain-lessons
Building a blockchain, one step at a time.

Chat with us on Discord, in our BlockChange Discussion group.
 
 https://discord.gg/vFeZuYj

## One might ask why should we build our own step by step. 

I can say that learning the process sometime can help better what exists.

## Getting Started

In our first lesson we just build our basic chain classes, and create an application to simulate the chain.

So what do we need ?

We need to record user transactions.
We need a way to associate those transactions to a wallet, so we will need a wallet as well.
We need to confirm and verify those transactions.
We also need to store these transaction in a block, once they have been confirmed, so we will need to build a miner as well as confirmation.


Lets start with the transacitons.


## The Transactions

We know we need an amount, we should include who its going to, and who we are. We will need to add confirmations, and we need to independantly verify it.

```JavaScript
{
    amount,
    sender,
    receiver,
    confirmations,
    verified
}

```

We almost have all the data we need, lastly we add our security measures.

```JavaScript
{
    amount,
    sender,
    receiver,
    confirmations,
    verified
    signature
}

```

As you can see we add a signature.
This is part of our security and Ill explain how later. 

```JavaScript
{
    amount,
    sender,
    receiver,
    confirmations,
    verified,
    signature
}

```

Now, we have our transactions layed out, lets figure out our blocks.

## The Block
```JavaScript
{
    block_no,
    transactions,
    previousHash,
    hash,
    proof,
    minedBy,
    value,
    listedBy,
    confirmations,
    verified,
    signature
}

```

Now that we have our basic data stuctures, we can figure how we need to access them.
Lets start with some of our basic blockchain interactions.


1) List Blockchain
    We need a way to list the blockchain. 
    We should consider there maybe lots of blocks, so we should handle them in sections.

2) List The Last Block
    List the last block that was forged.

3) Get A Wallet Balance
    Get the balance of a wallet if it exists on the chain.

4) List A Wallets Transactions
    List all of the recieve, sent, and awards.

5) List the Current Circulation
    This should be the total of all the mined awards for the entire chain, creating the total circulation.

6) Add a Transaction
    This should be a public route that any one can post a transaction to sending another address the transaction.

7) Add a Block
    This is so a miner can add the new block to the chain.

8) Confirm A Transaction
    Once a wallet submites a transaction the node will seek confirmations that others have it listed.

9) Confirm A Block
    Once a Block is forged the node will seek confirmations that it was listed.

    Notes :: This is an example of a way to do blockchain, and should not be used in a production environment with out being tested thourghly. Like the wheel blockchain is undergoing growth. Developers are working to create better blockchains that have more use than just to transact currency. 

Some idea's to think about when thinking of what can blockchain do for my company?

When you consider security being an issue, and giving away rewards that are often conterfieted creating blockchain integrated award systems. Store receipt of the transaction in all of your stores, or in just one.

With store houses full of Invoices and statements, you can now digitize these into smart contracts and store them on the blockchain.

More so, decentralizing data across the network of devices in a corporation can allow for more secure data management. 







