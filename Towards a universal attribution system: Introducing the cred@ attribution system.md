---
title: Towards a universal attribution system - Introducing the cred@ attribution system
date: 2024-11-24
tags: [attribution, cred@, open-protocol]
---

# Towards a universal attribution system: Introducing the cred@ attribution system

For some time now, I've wanted to create a system that would allow anyone to credit anyone for anything. I had the initial idea years ago, registered the https://cred.at domain, then just sat on the idea.

The initial idea was for a dumb simple, single line of text where you would do something like:

```
lux@cred@mom "best apple pie ever"
```

In this case, 'lux' would have given credit to 'mom' for making a great apple pie. At http://cred.at/lux/given, lux would see a list of credits he gave, and at http://cred.at/mom/credits/roll, mom would be happy to have credit for the great pie, and all the other credits.

I shelved this idea because it felt too broad, too stupid, too many issues with implementation, etc, etc, but I never was completely able to drop the idea.

Later I thought about using cred.at as a sort of "belief network", that would use natural language processing to determine attributions, so things like user@cred@historical_figure might be possible. For instance, the NLP processor would produce things like lux@cred@columbus "discovered America" while another user someoneelse@cred@vikings "discovered America". This would be a way to track beliefs and attributions through time, to understand why people believed the things they do, and where there is divergence. I think this is still an interesting idea that someone should definitely pursue and be implemented somehow, but again, it felt too broad.

Recently, especially in light of data needs for the AI/ML revolution, I'm seeing a need to have a way to attribute across systems.

For instance, you might want to attribute a research paper in arxiv, but implicit in that attribution, you are attributing the work of several authors, you are also attributing the work in their github repo, some related tweets on x (formerly twitter), some bluesky posts, etc etc.

There's also need to attribute sources in AI model training data as well, and a need to attribute artists for their work, etc etc. Also, for the purpose of machine understanding, it would be great to have a system where the LLM could easily track down the root of an idea, tracing, through the whole historical attribution chain in one fell swoop.

All the current systems for doing this are locked into one platform or another: there's issues of data control, verification, deleted information, etc.

This is why I think it's time for a system that is universal, open, distributed, optional, verifiable, platform independent and dead simple to use. I hope to make that system a reality here.

I've started a github repo to start building out the protocol syntax and initial backend (don't get too excited: still just a README doc, but go star it anyway).

I will be building the first implementation at https://cred.at, that will allow users to link their identities on various platforms and have a universal "inbox" for receiving cred@, but my goal here is to make a system where anyone can implement their own cred@ system if they like, and it will be interoperable with any other.

If you are a researcher, developer, or just someone who wants to give a cred@ to a friend on twitter, and are interested in being an early adopter, definitely reach out and let me know. It's totally minimal effort, you'll just get an account on cred.at, a place to host a blog, and the ability to give and receive cred@.

If you understand the implications and value of a system like this, early stage investment is also welcome... in either case, feel free to reach out to me on github, twitter or bluesky.

Thanks for reading! I'm also going to post some amazing AI/ML ideas on this blog as well, so visit again soon. Here's the general outline:

## Overview

cred@ is an open, distributed attribution system designed to create verifiable chains of intellectual credit across platforms and mediums. It provides: 

- Universal syntax for attribution 
- Verifiable credit chains 
- Automated tracking 
- Distributed verification 
- Platform independence

The system allows both passive tracking of attribution and active user engagement, while remaining platform-agnostic and open source.

## Basic Syntax

Core required elements:

```
cred@system:resource:unique_id
```

Full syntax with optionals:

```
[creditor]@cred@system:resource:id[:user][:temporal]
```

- **system**: The platform/source (arxiv, github, etc.)
- **resource**: Type of thing being credited (paper, repo, tweet, etc.)
- **id**: Unique identifier within that system
- **user**: Optional specific attribution (defaults to all contributors)
- **temporal**: Optional version/time reference (defaults to latest)

## System Examples

### Academic Papers

```
# Basic paper citation
cred@arxiv:paper:2311.12345

# Specific version/author
cred@arxiv:paper:2311.12345:hinton:v2

# DOI reference
cred@doi:paper:10.1038/nature12345
```

### Code/Software

```
# Repository
cred@github:repo:user/project

# Specific file
cred@github:file:user/repo/path/file.py

# Specific commit
cred@github:repo:project:user:commit-a1b2c3
```

### Social Media

```
# Tweet reference
cred@x:tweet:123456

# Blog post
cred@medium:post:user/post-id

# Video content
cred@youtube:video:video-id:timestamp
```

### Art/Creative Works

```
# Digital art
cred@opensea:artwork:token-id

# Music
cred@spotify:track:track-id

# Photography
cred@flickr:photo:photo-id
```

## Use Cases

### Passive Attribution

- Automatic citation tracking
- Work preservation
- Attribution chain mapping
- Timestamp verification

### Active User Features

- Identity unification across platforms
- Attribution "inbox" at cred.at/receive/username
- Credit visualization
- Impact metrics
- Connection graphs

### Tool Integration

- Document editor integration
- Citation management
- Rich web previews
- Development tool tracking
- AI/ML attribution

### AI/ML Applications

- Training data attribution
- Source verification
- Hallucination reduction
- Knowledge graphing
- Fact checking

## Distributed System Architecture

### Core Components

- Open Protocol
- Standard specification
- Reference implementation
- API definitions
- Verification methods

### Node Types

- Full nodes (complete data)
- Light nodes (recent data)
- Archive nodes (historical)
- Verification nodes

### Data Distribution

- Peer-to-peer sync
- Merkle tree verification
- Multiple redundant storage
- Decentralized consensus

## Implementation Approach

### Initial Phase

- Central cred.at service
- Basic API and tools
- Reference implementations
- Early adopter integration

### Decentralization

- Multiple independent nodes
- Distributed verification
- Community governance
- Open source tools

### Ecosystem Growth

- Third-party implementations
- Tool integration
- AI/ML adoption
- Standard establishment

## Future Development

### Priority Areas

- Core Protocol Development
- Reference Implementation
- API Standards
- Verification Systems
- Tool Integration

### Community Goals

- Open source development
- Distributed control
- Universal accessibility
- Transparent operation
- Sustainable growth

## Benefits

### Attribution

- Clear credit chains
- Verifiable sources
- Permanent records
- Cross-platform tracking

### Verification

- Timestamp proof
- Content preservation
- Attribution verification
- Chain validation

### Access

- Open protocol
- Free usage
- Universal standard
- Platform independent

### Intelligence

- Knowledge graphs
- Impact tracking
- Influence mapping
- AI/ML integration
