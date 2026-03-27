# GitHub Copilot CLI

## Bootstrap Prompt

### Step 1: Setup the Instructions

I want you to create an Azure policy so that if a resource group has a tag called "propogate" with a value of "true", then anytime a child resource gets created in that resource group, you will tag those resources with a tag "propogated" and value of "confirmed". Create this as a json file and save it in the /policy folder - you can create the /policy folder if it doesn't already exist.

### Step 2: Launch GitHub Copilot

```bash

# It is good to do this right away
az login

# Launch GitHub Copilot CLI
copilot --yolo

# Log into GitHub
> /login

# Initialize the session with prompt from above
> /init

# Add plugins if desired

# Microsoft Work IQ
> /plugin marketplace add github/copilot-plugins
> /plugin install workiq@copilot-plugins 

# Microsoft Learn Docs
> /plugin marketplace add microsoftdocs/mcp
> /plugin install microsoft-docs@microsoft-docs-marketplace

```

### Step 3: Possible MCP Servers

- **Azure MCP** - `npx -y @azure/mcp@latest server start`
- **Microsoft Fabric** - `npx -y @microsoft/fabric-mcp@latest server start --mode all   `
- **Playwright** - `npx -y @playwright/mcp@latest`
- **Azure DevOps** - `npx -y @azure-devops/mcp your-org-name`
