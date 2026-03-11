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
export ALICLOUD_ACCESS_KEY_ID="your-ak"
export ALICLOUD_ACCESS_KEY_SECRET="your-sk"
export ALICLOUD_REGION_ID="cn-shanghai"
```

4. Use the discovery scripts to explore available APIs:

```bash
cd skills/dataworks/open-api
python scripts/fetch_api_overview.py
python scripts/list_openapi_meta_apis.py
```

## Links

- [DataWorks Documentation](https://www.alibabacloud.com/help/dataworks)
- [OpenAPI Explorer](https://api.aliyun.com/product/dataworks-public)
- [DataWorks MCP Server (npm)](https://www.npmjs.com/package/alibabacloud-dataworks-mcp-server)
- [DataWorks MCP Server (GitHub)](https://github.com/aliyun/alibabacloud-dataworks-mcp-server)

## License

This project is licensed under the [Apache License 2.0](./LICENSE.txt).
