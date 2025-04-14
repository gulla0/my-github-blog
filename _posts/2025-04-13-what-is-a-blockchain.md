---
layout: post
title: "Part 2: Okay… So What Is a Blockchain, Really?"
date: 2025-04-13
thumbnail: assets/images/2.png
---
<p align="center">
  <img src="/my-github-blog/assets/images/2.png" alt="Journey begins" width="60%">
</p>

> **TL;DR:** A blockchain is a distributed ledger that enforces rules through consensus, creates immutability through cryptographic linking, and resists tampering through economic incentives.

<span class="first-letter">I</span> don't even remember when I first heard the word *blockchain*. It was just… around. One of those buzzwords that kept showing up — in crypto stuff, on random YouTube videos, or people acting like they knew what it meant.

At some point I stopped brushing it off and thought:  
**"Okay wait — what actually is a blockchain?"**

Not the fancy definitions. Just… how does it work?  
Who runs it? And why does everyone say it can't be changed?

That's when things got interesting.  
It didn't all click right away. It still hasn't fully. But slowly — in time — it started to make sense.

---

## Table of Contents
- [My Working Definition](#my-working-definition)
- [Valid or Not Valid — That's the Logic](#valid-or-not-valid--thats-the-logic)
- [It's the Nodes That Enforce the Rules](#its-the-nodes-that-enforce-the-rules)
- [What If a Node Tries to Cheat?](#what-if-a-node-tries-to-cheat)
- [Why It Rarely Happens Anyway](#why-it-rarely-happens-anyway)
- [But Can It Be Changed Later?](#but-can-it-be-changed-later)
- [The Hash That Holds Everything Together](#the-hash-that-holds-everything-together)
- [Why It Actually Works](#why-it-actually-works)
- [Final Thoughts](#final-thoughts)

---

## 🧠 My Working Definition

At this point, I'd probably describe a blockchain like this:

It's a **ledger** — a record of what happened.  
But not just any ledger. It's also a kind of **state machine** — meaning the state of things (who owns what, what contracts exist, what data lives on-chain) can be updated by something called a **transaction**.

And that transaction?  
It doesn't just change the state automatically.  
It gets checked first.

> A blockchain isn't just a database. It's a system that remembers in a way that's nearly impossible to fake or erase.

## ✅ Valid or Not Valid — That's the Logic

This is the part that started to make sense to me:

The chain doesn't just store stuff.  
**It makes decisions.**

And those decisions are simple: valid or not valid. Just booleans.

It's like the whole system runs on yes or no:  
Is this allowed?  
Does this follow the rules?

Back when I was first trying to understand how a blockchain works, I had this picture in my head:

> The chain itself was the thing making decisions.

Like it was this self-aware ledger that just *knew* if a transaction was valid or not. If it followed the rules, it got added. If not, it was rejected. Simple.

And honestly? That's not totally wrong.

## 🖥️ It's the Nodes That Enforce the Rules

Later I found out it's not really the chain that decides — it's the **software running on all these computers** around the world. The Cardano node software, in this case.

That software is what checks the rules, runs the logic, and says "yes" or "no."

But even though anyone can run the node software, not everyone gets to add blocks. That job rotates — an algorithm (**Ouroboros**) picks which computer (slot leader) gets to produce the next block.

But here's the important bit:

> Even if one node creates the block, every other node still verifies it.

That's what keeps things honest.  
The decision isn't made by a single authority — it's **cross-checked by thousands**.

## ❌ What If a Node Tries to Cheat?

I used to think the system somehow prevented bad blocks from being created at all.

Like, surely the software stops you from even minting an invalid block, right?

Nope.

A node that gets picked can still create a bad block — maybe by mistake, maybe on purpose. It can include invalid transactions, break the rules, whatever.

**But the network just won't accept it.**

> The rest of the nodes will say:  
> *"Nope. Doesn't follow the rules. I'm not adding this to my copy of the chain."*

So it's not about **stopping bad data at the source**, it's about **refusing to accept garbage**.

And that's the power of it.

## 💡 Why It Rarely Happens Anyway

In Cardano, this kind of bad behavior is rare.  
Slot leaders usually run stake pools. If they mess up too much, people stop delegating to them.

No delegation = no rewards = no incentive to cheat.

So the system is self-correcting — not perfect, but resilient.

## 🔒 But Can It Be Changed Later?

That led to my next question:  
**"What if someone wants to change it later?"**

What if they made a mistake? Or wanted to cheat after the fact?

That's where I started hearing about **immutability** — the idea that once something is on the blockchain, it can't be changed.

At first it felt like marketing. Nothing is truly unchangeable… right?

But the more I learned, the more I realized:  
It's not just a slogan — it's **baked into how the blockchain works**.

## 🧱 The Hash That Holds Everything Together

Each block includes a hash of the previous block — like a fingerprint.

If you change anything in a block — even a single character — that hash breaks.

And that breaks every block that comes after it.

As I put it to myself:

> *"No matter which block you change, every block that comes after changes."*

So to change one transaction, you'd have to rewrite the whole chain from that point forward.

And convince the network to go along with your version.

That's… not going to happen.

## 🔐 Why It Actually Works

Even if you tried to fake history:

1. It's **unprofitable**  
2. It's **visible**  
3. It's **technically hard**

So yeah — the immutability thing?  
It's real. Not just marketing.

## 🧠 Final Thoughts

That's when blockchain stopped being an abstract idea for me.  
Not just coins or smart contracts or tokens.

It's a **system that remembers**.  
And it remembers in a way that's nearly impossible to fake or erase.

I'm still figuring things out. There's a lot I don't fully understand yet.

But compared to when I started?

Yeah — the fuzziness is lifting a bit.

---

*If you enjoyed this article, you might also like [Becoming a Builder: My Cardano Journey](/my-github-blog/2025-04-13-cardano-journey-part-1)*

---

*Just someone learning blockchain one step at a time. Follow my journey as I explore the technology behind Cardano and other blockchains.*
