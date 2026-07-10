---
title: Sysmon Log Parser
summary: A Python tool for parsing and normalizing Sysmon event logs to speed up detection engineering and threat hunting.
tags: [Detection Engineering, Python, Sysmon]
github: https://github.com/CyberSecKat/REPLACE_WITH_REPO_NAME
date: 2026-07-09
---

<!-- PLACEHOLDER: replace with a real writeup of the project — what problem
     it solves, how it works, and what you learned building it. -->
A command-line tool that parses raw Sysmon event logs (EVTX/XML/JSON) into a
normalized, queryable format, making it faster to build and test detection
logic against real telemetry.

## Why I built it

Sysmon produces rich telemetry, but working with raw event XML is slow going
when you're iterating on detection logic. This tool flattens and normalizes
the fields that matter most for detection engineering, so I can pipe parsed
events straight into analysis or test harnesses instead of hand-parsing XML.

## Highlights

- Normalizes common Sysmon event IDs (process creation, network connections,
  file creation, registry events) into a consistent schema
- Outputs to JSON/CSV for easy loading into pandas, a SIEM, or a notebook
- Built with extensibility in mind — new event types are easy to add

Check out the full source and README on GitHub for setup and usage details.
