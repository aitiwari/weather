# Firecrawl MCP Server Integration with Cursor IDE

This guide provides step-by-step instructions on how to set up and use the Firecrawl MCP Server with Cursor IDE. Follow the steps below to integrate Firecrawl's web scraping capabilities into your Cursor environment.

---

## Prerequisites
1. **Firecrawl API Key**: Required to authenticate and use Firecrawl services.
2. **Cursor IDE**: A code editor with AI capabilities.

---

## Step 1: Obtain a Firecrawl API Key
To get your Firecrawl API key, follow these steps:

1. **Sign Up or Log In**:
   - Visit the official Firecrawl website at [firecrawl.dev](https://www.firecrawl.dev).
   - Log in using your credentials or sign up if you are a new user. You can use Google Sign-In for a quick setup.

2. **Access the Dashboard**:
   - After logging in, you will be redirected to your dashboard.

3. **Locate the API Key**:
   - On the dashboard, find the API key section. It is typically located on the top-right side or in the settings panel.

4. **Copy Your API Key**:
   - Click on the API key to copy it. You will use this key for integration with Firecrawl services.
   ![firecrawl_mcp_server](screenshot\firecrawl_mcp_server.png)

---

## Step 2: Get MCP Server Configuration File in JSON Format
1. Open the link: [https://mcp.so/server/firecrawl-mcp-server?tab=tools](https://mcp.so/server/firecrawl-mcp-server?tab=tools).
2. Paste the Firecrawl API key obtained in Step 1 into the designated field as shown in the screenshot.
   ![firecrawl_mcp_server](screenshot\firecrawl_mcp_server.png)

3. To connect with the **Connect Server with SSE URL**, use the following configuration in JSON format:

   ```json
      {
         "mcpServers": {
            "@mendableai/firecrawl-mcp-server": {
               "url": "https://router.mcp.so/sse/2rbxtXXXXXXXXXX"
            }
      }
   }
   ```

   ![Cursor_mcp_config_json](screenshot\Cursor_mcp_config_json.png)

4. **Note**: You can also obtain the MCP server configuration to use as a tool in Claude Desktop, as shown in the screenshot.

---

## Step 3: Download and Install Cursor IDE
1. Download Cursor IDE from the official website: [https://www.cursor.com/en](https://www.cursor.com/en).
2. Install Cursor with the default settings.

---

## Step 4: Set Up Firecrawl MCP Server in Cursor
To configure the Firecrawl MCP Server in Cursor, follow these steps:

1. Open Cursor and go to **Settings > Cursor Settings**.
2. Find the **MCP Servers** option and enable it.
3. Click **"Add new MCP server"** or **"Add new global MCP server"**.
4. In the configuration window, paste the JSON configuration obtained in Step 2.
5. Replace the placeholder API key with your actual Firecrawl API key.
6. Save the settings. If configured correctly, you should see a green indicator light, showing that the Firecrawl MCP server is active and ready to use.

**Troubleshooting**:
- If the indicator doesn't turn green:
  - Restart Cursor.
  - Double-check your API key.
  - Press the refresh button in the MCP server settings.

---

## Step 5: Test the MCP Server in Cursor
Once the Firecrawl MCP Server is set up, you can test it as a tool in Cursor:

1. Open or create any file in Cursor.
2. Press `Ctrl + I` to open a new chat.
3. Ask the AI:  
   **"Use Firecrawl to scrape the title from @https://krishnaikacademy.com/"**.

This will demonstrate the integration and functionality of the Firecrawl MCP Server within Cursor.

![Cursor_mcp_test](screenshot\Cursor_mcp_test.png)

---

## Additional Notes
- Ensure your Firecrawl API key is kept secure and not shared publicly.
- For advanced configurations or troubleshooting, refer to the official Firecrawl and Cursor documentation.

---

Enjoy enhanced web scraping and data extraction capabilities with Firecrawl MCP Server and Cursor IDE!