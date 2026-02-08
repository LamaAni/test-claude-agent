# Agent Specification

## Directory Structure
```
/project-root/
├── /agents/
│   ├── agent1/
│   ├── agent2/
│   └── agentN/
├── /skills/
│   ├── skill1/
│   ├── skill2/
│   └── skillN/
├── /rules/
│   ├── rule1/
│   ├── rule2/
│   └── ruleN/
└── /configs/
    └── config.yaml
```

## Execution Flow
### Agent Discovery and Selection
- **Single Agent Mode**: Describe how a single agent is selected based on certain criteria.
- **Combined Agent Mode**: Describe the logic for selecting multiple agents and how they interoperate.

### Six-Phase Execution Flow
1. **Initialization**: Explain the setup required before the agent starts execution.
2. **Rule Validation**: Describe how rules are validated for execution.
3. **Skill Lookup**: Explain how and where skills are looked up.
4. **Configuration Loading**: Describe how configurations are loaded and used.
5. **Scope Determination**: Explain how the agent determines what tasks it should focus on.
6. **Execution**: Describe how the final execution is carried out.

## Shared vs Agent-Specific Skills and Rules
- **Shared Skills**: Define skills that can be accessed by all agents.
- **Agent-Specific Skills**: Define skills that are unique to individual agents.
- **Shared Rules**: Define rules that apply across all agents.
- **Agent-Specific Rules**: Define rules that are unique to specific agents.