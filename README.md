# agent-portfolio

## Purpose

This agent tracks asset holdings across multiple platforms and wallets.  
It provides visibility into exposure, performance, and allocation.  
The goal is to support informed rebalancing, monitoring, and reporting  
within an automated investment system.

## Responsibilities

- Aggregate balance and position data from exchanges and wallets  
- Calculate overall portfolio value and asset allocation  
- Track historical performance over time  
- Flag anomalies such as sudden drawdowns or imbalances  
- Summarize exposure by asset, platform, or tag

## Inputs

- Exchange APIs and wallet interfaces for balance queries  
- Configuration files defining portfolio structure or grouping  
- Execution records from agent-trade  
- Metadata from agent-exchange for platform context

## Outputs

- Portfolio snapshots with balance, value, and allocation  
- Historical logs for performance tracking  
- Flags or alerts for significant changes  
- Reports for human review or input to other agents

## Update Triggers

- Scheduled periodic refresh  
- Trade completion from agent-trade  
- Manual update trigger for sync

## Design Principles

- Passive monitoring with high reliability  
- Modular input structure to support new platforms  
- Output formats usable by both humans and agents  
- Low-latency updates, but not real-time trading frequency

## Change Logging

Track and log:

- Daily portfolio value  
- New assets or removed assets  
- Unusual value shifts or drawdowns  
- Rebalancing events or manual changes

## Integration

- Receives updates from agent-trade and external APIs  
- Informs investor-index of portfolio health  
- Provides input to planners or reviewers in multi-agent workflows

## Status

This document defines the full planning and operational scope for `agent-portfolio`.  
No separate PRD is needed.
