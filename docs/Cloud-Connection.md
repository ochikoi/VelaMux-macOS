# Cloud Connection

VelaMux works locally without any account. Cloud access is optional: it lets a cloud agent, such as ChatGPT, use VelaMux on your Mac through your own private tunnel.

## What you need

- An OpenAI Platform tunnel and its **Tunnel ID**
- A **Runtime API key** for the same organization
- The tunnel linked to the ChatGPT workspace you'll use

See OpenAI's guide: https://developers.openai.com/api/docs/guides/secure-mcp-tunnels

Use your own key only. Use a separate tunnel for each Mac.

## Set up

1. Double-click **Install VelaMux.command**.
2. Choose **Local + cloud install**, or **Add cloud to an existing local install** if VelaMux is already installed.
3. Enter your Tunnel ID and Runtime API key when asked.

The key is stored only on your Mac. Your local MCP port is never opened to the internet.

## Connect in ChatGPT

In ChatGPT developer mode, create a connector, choose **Tunnel**, and select your tunnel. If it isn't listed, check that the tunnel is linked to your workspace and that you have permission to use it.

If you get a 401 or 403 error, check your key and account permissions; reinstalling won't help.
