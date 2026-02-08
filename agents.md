# Agents Logic and Configuration

> **📋 USER INTERACTION GUIDE**  
> When a user says **"Load agents.md"** or **"Act as agents.md"**, present this menu:
> 
> ```
> 🤖 Agent System Loaded
> 
> What would you like to do?
> 
> 1. List agents I can act as
> 2. Act as all agents
> 3. Create and manage an agent
> 
> Please choose an option (1-3) or describe what you need.
> ```
> 
> **IMPORTANT**: Only show the menu above. Do NOT print the entire file contents, explanations, summaries, or any other information unless the user specifically requests it.

---

This file defines the logic of what an agent is, how agents work, and how they are managed in this repository.

## Repository Structure

```
/project-root/
├── agents.md         - This file: Defines the logic of what an agent is
├── README.md         - Repository documentation
├── /agents/          - Each agent in its own directory (agent-specific resources)
│   └── /agent_name/
│       ├── agent.md  - Main agent definition (mostly references to other files)
│       ├── README.md - Agent documentation
│       └── ...       - Any agent-specific files (rules, config, personas, etc.)
├── /skills/          - Shared skills available to all agents (single file per skill)
│   └── skill_name.md
├── /rules/           - Shared rules that apply across agents (single file per rule)
│   └── rule_name.md
└── /configs/         - Shared configuration files
    └── config.yaml
```

## File Organization Principles

### Agents
- **Agents have their own directory** with multiple possible files
- Agent directories can contain any files the agent needs:
  - `agent.md` - Main agent definition (acts as index/entry point, mostly contains references)
  - `README.md` - Agent documentation
  - Additional files: rules, configs, personas, examples, etc.
- **No restrictions** on what can be in an agent's directory

### Everything Else (Skills, Rules, Configs)
- **Single file per item** (not in subfolders unless specifically needed)
- Examples:
  - Skills: `/skills/self_update.md`
  - Rules: `/rules/validation.md`
  - Configs: `/configs/config.yaml`

## Agent Discovery and Selection

After this agents file is loaded, users are presented with a "menu" to choose which agent to use:

- **Single Agent Mode**: User selects one agent based on criteria/menu options
- **Combined Agent Mode**: User selects multiple agents that work together with interoperability logic

## Agent Loading (Done Once)

Loading the agent means loading the agent.md file. which define what the agent does, and following references if needed.

**Steps:**
1. **Initialization**: Setup required before the agent starts
2. **Configuration Loading**: Configurations loaded once when agent is loaded
3. **Scope Determination**: Agent determines its focus area once when loaded

## Agent Querying (Per Conversation Turn)

Querying the agent means interacting with the current state of the agent per the conversation.

**This is a separate flow with its own steps:**
1. **Rule Validation**: Rules validated for the query
2. **Skill Lookup**: Skills looked up as needed for the query
3. **Execution**: Final execution carried out for the query

## Shared vs Agent-Specific Resources

### Shared Resources
- **Shared Skills**: Available to all agents (located in `/skills/`)
- **Shared Rules**: Apply across all agents (located in `/rules/`)
- **Shared Configs**: Available to all agents (located in `/configs/`)

### Agent-Specific Resources
- **Agent-Specific Files**: Any files within an agent's directory
  - Can include: rules, configs, personas, documentation, examples, etc.
  - Accessible only to that specific agent

## Agent Definition Structure

An `agent.md` file should:
- Act as the **entry point** for the agent
- Contain **mostly references** to other files
- Include basic topics and overview
- Point to:
  - Specific rules (shared or agent-specific)
  - Skills the agent uses
  - Personas or style guides
  - Configuration files
  - Other files that define resources.
  - Any other relevant resources

## Creating New Agents

When creating a new agent:
1. Create a new directory in `/agents/` with the agent name
2. Create an `agent.md` file as the main definition
3. Create a `README.md` file for documentation
4. Add any additional files needed (personas, rules, configs, etc.)
5. Reference shared skills and rules as needed
6. Ensure the agent follows the principles defined in this file