# AI Coding Toolkit for Plaid

A comprehensive toolkit designed to accelerate Plaid integration development using AI coding assistants. This repository provides sandbox MCP tools (mock data generation, documentation search capabilities, webhook simulation, and more).

## Quick Start

### Prerequisites
- Python 3.10+
- uv (package manager)
- Plaid API credentials (for production use)

### Installation

```bash
# Clone the repository
git clone https://github.com/fabianathaydesr2/ai-coding-toolkit.git
cd ai-coding-toolkit

# Install dependencies
cd sandbox
uv sync

# Set environment variables (for production)
export PLAID_CLIENT_ID="your_client_id"
export PLAID_SECRET="your_secret"

# Run the MCP server
python -m mcp_server_plaid
```

### Quick Verification

```bash
# Verify installation
python -c "import mcp; print(f'✓ MCP version: {mcp.__version__}')"

# Run tests
pytest

# Start the server
python -m mcp_server_plaid --help
```

## Troubleshooting

### Module not found errors
```bash
# Ensure you're in the sandbox directory and dependencies are synced
cd sandbox
uv sync --refresh
```

### Permission errors
```bash
# Set proper permissions for the .env file
chmod 600 .env
```

### Server won't start
```bash
# Check for port conflicts
lsof -i :8000

# Verify Plaid credentials are set correctly
echo $PLAID_CLIENT_ID
echo $PLAID_SECRET
```

## Repository Structure

- `/sandbox`: Contains a sandbox MCP server implementation that helps developers integrate with Plaid more quickly by providing mock data and sandbox API access.
- `/rules`: Contains product-specific guides that can be used either as direct prompts for AI assistants or as Cursor rules to accelerate Plaid integration development.

## Sandbox MCP Server

The sandbox MCP server located in `/sandbox` directory provides a set of tools to facilitate faster integration with Plaid. It offers:

- Mock financial data generation
- Plaid documentation search
- Sandbox API access tokens
- Webhook simulation

This sandbox environment allows developers to test their Plaid integrations without using real financial data.

### Key Features

- **Generate mock financial data** for testing purposes
- **Search Plaid documentation** for relevant API information
- **Obtain sandbox access tokens** for testing
- **Simulate webhooks** to test application handling

### Getting Started

To use the sandbox MCP server, navigate to the `/sandbox` directory and follow the instructions in its README.

```bash
cd sandbox
# Follow instructions in sandbox/README.md for setup and usage
```

## Rules for AI Integration

The `/rules` directory contains comprehensive guides for various Plaid products and features. These guides can be used in two ways:

1. **Direct Prompts**: Copy the content directly into your conversations with AI assistants to provide them with specialized knowledge about Plaid products.

2. **Cursor Rules**: Import them as Cursor rules to enable your AI coding assistant to automatically understand Plaid's integration patterns and best practices.

Using these rules significantly accelerates development by giving AI models the context they need to generate code for Plaid integrations.

> [!WARNING]
These guides are designed to be used for the purpose of building a sample Plaid integration with the use of AI coding tools. You are solely responsible for ensuring the correctness, legality, security and performance of your code and integrations. These guidelines are provided "as-is" without any warranties. Use them at your own risk and discretion.

## Recent Updates

### Dependencies Updated (v2.0.0)
- **mcp**: 1.6.0 → 1.23.0 (Latest MCP spec 2025-11-25)
- **starlette**: 0.46.1 → 1.0.1 (**STABLE RELEASE** 🎉)
- **pytest**: 8.3.5 → 9.0.3 (Security fixes)
- **urllib3**: 2.4.0 → 2.7.0 (Security patches)
- **python-dotenv**: 1.1.0 → 1.2.2 (Python 3.14 support)
- **h11**: 0.14.0 → 0.16.0 (Validation improvements)
- **idna**: 3.10 → 3.15 (Unicode 17.0.0 support)

**Security Highlights:**
- ✅ urllib3 2.7.0: Fixed decompression-bomb vulnerabilities (GHSA-mf9v-mfxr-j63j)
- ✅ pytest 9.0.3: Fixed insecure temporary directory (CVE-2025-71176)
- ✅ idna 3.15: Resolved CVE-2026-45409 quadratic time processing

## License

This project is licensed under the MIT License - see the LICENSE file for details.
