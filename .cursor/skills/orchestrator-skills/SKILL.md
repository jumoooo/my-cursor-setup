---
name: orchestrator-skills
description: Core functions for Orchestrator agent - request analysis, agent selection, task distribution, conflict detection, multi-agent coordination. Use when orchestrating complex or multi-step tasks, distributing work across agents, or coordinating multiple agents.
---

# Orchestrator Skills

## Language Separation
**Internal (Agent reads)**: English. **User-facing**: Korean.

## Overview

Core functions for Orchestrator: request analysis, agent selection, task distribution, conflict detection, multi-agent coordination.

## Skills

### 1. Analyze User Request
Parse request, classify task type, assess complexity, identify required capabilities and dependencies.

### 2. Discover Available Agents
List `.cursor/agents/`, extract name/description/capabilities/triggers from each agent file.

### 3. Select Appropriate Agent(s)
Match task requirements with agent capabilities. Document selection reasoning.

### 4. Create Distribution Plan
Define task sequence, workflow, expected completion per agent.

### 5. Detect Agent Conflicts
Check for overlapping tasks, contradictory instructions, resource conflicts, dependency issues.

### 6. Generate Distribution Report
Create user-friendly report in Korean with confirmation request.

### 7. Coordinate Multi-Agent Tasks
Define execution order (sequential/parallel), data flow, coordination checkpoints.

### 8. Monitor Task Progress
Track completion status, report progress, identify blockers.

### 9. Update Agent Registry
When new agents are added, check conflicts and update registry.

## Usage Guidelines

- Always analyze request before distribution
- Always check for conflicts
- Always get user confirmation
- Always report in Korean
- Use Codebase Search / list_dir to discover agents

## Quality Standards

- Clear task classification
- Documented selection reasoning
- Korean user reports
- Conflict-free distribution
