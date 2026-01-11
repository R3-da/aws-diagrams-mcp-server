# AWS Diagrams MCP Server

## VS Code Setup

Copy the following configuration into your `mcp.json` file located in the `.vscode` directory:

```json
{
  "servers": {
    "Core MCP Server": {
      "command": "uvx",
      "args": [
        "awslabs.core-mcp-server@latest"
      ],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      },
      "autoApprove": [],
      "disabled": false,
      "type": "stdio"
    },
    "awslabs.aws-diagram-mcp-server": {
      "command": "uvx",
      "args": [
        "awslabs.aws-diagram-mcp-server"
      ],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      },
      "autoApprove": [],
      "disabled": false,
      "type": "stdio"
    }
  },
  "inputs": []
}
```

## Alternative Installation (Manual)

You can also install the MCP servers manually using the following links:

- **Core MCP Server**  
  https://insiders.vscode.dev/redirect/mcp/install?name=Core%20MCP%20Server&config=%7B%22command%22%3A%22uvx%22%2C%22args%22%3A%5B%22awslabs.core-mcp-server%40latest%22%5D%2C%22env%22%3A%7B%22FASTMCP_LOG_LEVEL%22%3A%22ERROR%22%7D%2C%22autoApprove%22%3A%5B%5D%2C%22disabled%22%3Afalse%7D

- **AWS Diagram MCP Server**  
  https://insiders.vscode.dev/redirect/mcp/install?name=AWS%20Diagram%20MCP%20Server&config=%7B%22command%22%3A%22uvx%22%2C%22args%22%3A%5B%22awslabs.aws-diagram-mcp-server%22%5D%2C%22env%22%3A%7B%22FASTMCP_LOG_LEVEL%22%3A%22ERROR%22%7D%2C%22autoApprove%22%3A%5B%5D%2C%22disabled%22%3Afalse%7D

## Example Prompt

The following prompt was used to generate the example AWS architecture diagram:

> Create an AWS data pipeline architecture diagram showing data producers streaming events into Amazon Kinesis Data Streams, processing and transforming the data using AWS Glue ETL, and loading the curated data into Amazon Redshift for analytics. The diagram should also include BI and reporting consumers and clearly illustrate the end-to-end data flow.