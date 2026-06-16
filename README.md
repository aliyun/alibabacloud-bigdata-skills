# Try DataWorks Agent

Want a ready-to-use AI experience for DataWorks without manual setup?

**[DataWorks Agent](https://dataworks.data.alibabacloud.com/product/agent?source=github)** is Alibaba Cloud's built-in intelligent assistant for data development and operations. It connects to your DataWorks workspace out of the box, so you can use natural language to explore metadata, develop nodes, troubleshoot tasks, and manage resources—no local MCP server or skill configuration required.

| | DataWorks Agent | Skills (this repo) | [DataWorks MCP Server](https://github.com/aliyun/alibabacloud-dataworks-mcp-server) |
| --- | --- | --- | --- |
| **Best for** | Quick start in the DataWorks console; also supports multiple big data skills such as Flink, EMR, Hologres, MaxCompute, and more | Teaching AI agents best practices for DataWorks Open API | Custom AI clients (Cursor, Cline, etc.) |
| **Setup** | Open and use in browser | Add skill to your agent's skill directory | Install, configure AK, and connect MCP |
| **Integration** | Native DataWorks experience | SDK-first workflows, API discovery scripts, cookbooks | Open API exposed as MCP tools |

👉 **Get started:** [https://dataworks.data.alibabacloud.com/product/agent?source=github](https://dataworks.data.alibabacloud.com/product/agent?source=github)

If you prefer embedding DataWorks capabilities into your own AI workflow or IDE, use the skills below or connect via the MCP Server.

# Alibaba Cloud Big Data Skills

A collection of AI agent skills for [Alibaba Cloud](https://www.alibabacloud.com/) big data services. Each skill is a self-contained package that teaches AI agents how to interact with specific cloud services.

## Available Skills

| Product | Skill | Description |
|---------|-------|-------------|
| DataWorks | [open-api](./skills/dataworks/open-api/) | Operate DataWorks through dynamic API discovery and official SDKs (Node.js, Python, Java). Covers data development, workflow operations, data integration, data quality, metadata lineage, workspace management, and more. |

## Repository Structure

```
alibabacloud-bigdata-skills/
├── README.md                            # This file
├── LICENSE.txt                          # Apache License 2.0
├── icon.png                             # Skill icon
├── icon-small.png                       # Skill icon (small)
└── skills/
    └── dataworks/                       # DataWorks product skills
        └── open-api/          # DataWorks Open API skill
            ├── README.md                # Skill overview and quick start
            ├── SKILL.md                 # Main skill instructions (read by AI agent)
            ├── agents/
            │   └── openai.yaml          # Agent interface definition
            ├── references/
            │   ├── sources.md           # API docs, SDK, and MCP Server links
            │   └── mcp_server.md        # MCP Server setup and configuration
            └── scripts/
                ├── fetch_api_overview.py     # Fetch API list from official help docs
                └── list_openapi_meta_apis.py # Fetch API specs from OpenAPI metadata
```

## Quick Start

1. Pick a skill from `skills/` (e.g. `skills/dataworks/open-api/`).
2. Read the `SKILL.md` inside — it contains all instructions an AI agent needs.
3. Set up credentials:

```bash
# Option A: Credentials URI (recommended for local development)
export ALIBABA_CLOUD_CREDENTIALS_URI="http://localhost:7002/api/v1/credentials/0"

# Option B: Static AK/SK
export ALIBABA_CLOUD_ACCESS_KEY_ID="your-ak"
export ALIBABA_CLOUD_ACCESS_KEY_SECRET="your-sk"

export ALIBABA_CLOUD_REGION_ID="cn-shanghai"
```

4. Use the discovery scripts to explore available APIs:

```bash
cd skills/dataworks/open-api
python scripts/fetch_api_overview.py
python scripts/list_openapi_meta_apis.py
```

## Links

- [DataWorks Agent](https://dataworks.data.alibabacloud.com/product/agent?source=github)
- [DataWorks Documentation](https://www.alibabacloud.com/help/dataworks)
- [OpenAPI Explorer](https://api.aliyun.com/product/dataworks-public)
- [DataWorks MCP Server (npm)](https://www.npmjs.com/package/alibabacloud-dataworks-mcp-server)
- [DataWorks MCP Server (GitHub)](https://github.com/aliyun/alibabacloud-dataworks-mcp-server)

## License

This project is licensed under the [Apache License 2.0](./LICENSE.txt).
