---
id: hyperexecute-mcp-server-release-notes
title: Version 1.131.0
hide_title: false
sidebar_label: Version 1.131.0
description: Version 1.131.0
keywords:
  - LambdaTest Hyperexecute
  - LambdaTest Hyperexecute help
  - LambdaTest Hyperexecute documentation
  - FAQs
url: https://www.lambdatest.com/support/docs/hyperexecute-mcp-server-release-notes/
site_name: LambdaTest
slug: hyperexecute-mcp-server-release-notes/
---

<script type="application/ld+json"
      dangerouslySetInnerHTML={{ __html: JSON.stringify({
       "@context": "https://schema.org",
        "@type": "BreadcrumbList",
        "itemListElement": [{
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://www.lambdatest.com"
        },{
          "@type": "ListItem",
          "position": 2,
          "name": "Support",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "Version",
          "item": "https://www.lambdatest.com/support/docs/hyperexecute-mcp-server-release-notes/"
        }]
      })
    }}
></script>


# MCP LambdaTest Release Notes

## Version 1.0.0 - Major Release

### 🎉 What's New

#### Rebranding & Package Updates

- **MCP Hyperexecute** is now **MCP LambdaTest** to better reflect our expanded capabilities
- Updated package name to `mcp-lambdatest` on NPM
- Stable 1.0.0 release with comprehensive feature set

#### Transport Support

- **STDIO Transport**: Available via NPM package for local installations
- **StreamableHTTP Transport**: Replaces deprecated SSE transport for remote connections
- Enhanced connection reliability and performance

#### Enhanced Migration Tools

- Expanded migration capabilities for easier transition to LambdaTest platform
- Improved app upload functionality for mobile testing
- Resolved template loading and asset management for migration tools

#### Security & Reliability Improvements

- Enhanced authentication mechanisms
- Improved credential handling and validation
- Better security practices for remote connections
- Fixed MCP resource loading issues for capabilities mapping and hooks executor
- Updated webpack configuration to properly copy JSON assets during build process

### 🔧 Connection Configuration

#### ⚠️ Breaking Changes

The previous SSE-based connection method has been **removed**:

```
❌ OLD (No longer supported):
http://mcp.lambdatest.com/hyperexecute?&username=[your-lt-username]&accessKey=[your-lt-access-key]
```

#### ✅ Connection Methods

**Option 1: Remote MCP Server (StreamableHTTP)**

```json
{
  "mcpServers": {
    "mcp-lambdatest-remote": {
      "disabled": false,
      "timeout": 60,
      "command": "npx",
      "args": [
        "mcp-remote@latest",
        "https://mcp.lambdatest.com/mcp",
        "--header",
        "username:<LT_USERNAME>",
        "--header",
        "accessKey:<LT_ACCESSKEY>"
      ],
      "transportType": "streamableHTTP"
    }
  }
}
```

**Option 2: Local STDIO Server (NPM Package)**

```json
{
  "mcpServers": {
    "mcp-lambdatest-stdio": {
      "disabled": false,
      "timeout": 100,
      "command": "npx",
      "args": ["-y", "mcp-lambdatest", "--transport=stdio"],
      "env": {
        "LT_USERNAME": "<LT_USERNAME>",
        "LT_ACCESS_KEY": "<LT_ACCESSKEY>"
      },
      "transportType": "stdio"
    }
  }
}
```

### 🚀 Getting Started

1. **Choose your connection method** (Remote or Local STDIO)
2. **Update your configuration** with the new format above
3. **Replace credentials** with your LambdaTest username and access key
4. **Verify connection** by asking your AI assistant to list available MCP tools
5. **Start using** LambdaTest tools directly within your AI assistant

### 📋 Available Tools

#### HyperExecute Tools

- **generateHyperExecuteYAML**: Generate YAML configurations for your test projects
- **answerHyperExecuteQuery**: Get answers from HyperExecute documentation
- **getHyperExecuteJobInfo**: Fetch detailed job information
- **getHyperExecuteJobSessions**: Retrieve job session details

#### Migration Tools

- **upload_app**: Upload mobile applications for testing

### 🔗 Compatibility

This release is compatible with:

- Cline (Claude Dev)
- Any MCP-compatible AI assistant
- Both local and remote deployment scenarios

### 📞 Support

For questions or issues with the connection methods, please refer to our documentation or contact LambdaTest support.

---

**Note**: Make sure to update your configurations to use the new connection methods as the old SSE-based approach is no longer supported.
