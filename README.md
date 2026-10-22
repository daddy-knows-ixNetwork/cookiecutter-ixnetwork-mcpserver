# cookiecutter-ixnetwork-mcpserver
cookiecutter template for IxNetwork MCP Server

## How to 

```
(.venv) $ cookiecutter .
  [1/12] IXNETWORK_MCP_SERVER_IMAGE (ixnetwork-mcp:26.0.0-147): 
  [2/12] IXNETWORK_MCP_HOST_PORT (9966): 
  [3/12] IXNETWORK_MCP_HOST_IP (172.21.191.86): 
  [4/12] IXNETWORK_MCP_ENABLE_TLS (true): 
  [5/12] IXNETWORK_MCP_LICENSE_SERVER (10.36.159.38): 
  [6/12] PUBLIC_BASE_URL (https://172.21.191.86:9966): 
  [7/12] IXN_USERNAME (admin): 
  [8/12] IXN_PASSWORD (admin): 
  [9/12] project_name (ixNetwork MCP Server Docker Compose): 
  [10/12] project_slug (ixnetwork-mcp-server-docker-compose): 
  [11/12] project_short_description (A cookiecutter template for IxNetwork MCP Server): 
  [12/12] first_version (0.1.0): 
(.venv) $ cd ixnetwork-mcp-server-docker-compose/
(.venv) ixnetwork-mcp-server-docker-compose$ docker compose up
[+] up 4/4
 ✔ Network ixnetwork-mcp-server-docker-compose_default           Created                                                                                      0.0s
 ✔ Volume ixnetwork-mcp-server-docker-compose_ixnetwork-mcp-data Created                                                                                      0.0s
 ✔ Volume ixnetwork-mcp-server-docker-compose_ixnetwork-mcp-logs Created                                                                                      0.0s
 ✔ Container ixnetwork-mcp-server                                Created                                                                                      0.0s
Attaching to ixnetwork-mcp-server
ixnetwork-mcp-server  | 2026-10-22 17:11:17,697 - ixnetwork-mcp - INFO - Log file: /var/log/ixnetwork-mcp/ixnetwork-mcp_2026-10-22_171117_20.log
ixnetwork-mcp-server  | 2026-10-22 17:11:17,698 - ixnetwork-mcp - INFO - ixnetwork-mcp version 26.0.0+147
ixnetwork-mcp-server  | 2026-10-22 17:11:17,700 - ixnetwork-mcp - INFO - Licensing configured: 10.36.159.38:7443 [IXN-MCP-BASEx1]
ixnetwork-mcp-server  | 2026-10-22 17:11:18,028 - ixnetwork-mcp - INFO - Licensing initialised against 10.36.159.38:7443 [IXN-MCP-BASEx1]
ixnetwork-mcp-server  | 2026-10-22 17:11:18,029 - ixnetwork-mcp - WARNING - SSE (multi-user) mode enabled. All tool calls require explicit session_id — auto-resolution is disabled.
ixnetwork-mcp-server  | 2026-10-22 17:11:18,029 - ixnetwork-mcp - INFO - PUBLIC_BASE_URL set to https://172.21.191.86:9966
ixnetwork-mcp-server  | 2026-10-22 17:11:18,029 - ixnetwork-mcp - INFO - sse_hooks: installed SSE disconnect hook on SseServerTransport.connect_sse
ixnetwork-mcp-server  | 2026-10-22 17:11:18,029 - ixnetwork-mcp - INFO - Starting IxNetwork MCP Server (transport=sse)
ixnetwork-mcp-server  | 2026-10-22 17:11:18,029 - ixnetwork-mcp - INFO - TLS enabled (ssl_certfile=/run/ixnetwork-mcp/certs/server-c19cdbb857125a14.crt)
ixnetwork-mcp-server  | 2026-10-22 17:11:18,030 - ixnetwork-mcp - INFO - SSE server listening on 0.0.0.0:8000
ixnetwork-mcp-server  | 
ixnetwork-mcp-server  | 
ixnetwork-mcp-server  | ╭──────────────────────────────────────────────────────────────────────────────╮
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | │                         ▄▀▀ ▄▀█ █▀▀ ▀█▀ █▀▄▀█ █▀▀ █▀█                        │
ixnetwork-mcp-server  | │                         █▀  █▀█ ▄▄█  █  █ ▀ █ █▄▄ █▀▀                        │
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | │                                FastMCP 4.0.5                                 │
ixnetwork-mcp-server  | │                            https://gofastmcp.com                             │
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | │                  🖥  Server:      IxNetwork-MCP, 4.0.5                        │
ixnetwork-mcp-server  | │                  🚀 Deploy free: https://horizon.prefect.io                  │
ixnetwork-mcp-server  | │                                                                              │
ixnetwork-mcp-server  | ╰──────────────────────────────────────────────────────────────────────────────╯
ixnetwork-mcp-server  | ╭──────────────────────────────────────────────────────────────────────────────╮
ixnetwork-mcp-server  | │                          🎉 Update available: 4.1.3                          │
ixnetwork-mcp-server  | │                      Run: pip install --upgrade fastmcp                      │
ixnetwork-mcp-server  | ╰──────────────────────────────────────────────────────────────────────────────╯
ixnetwork-mcp-server  | 
ixnetwork-mcp-server  | 
ixnetwork-mcp-server  | 2026-10-22 17:11:18,162 - ixnetwork-mcp - INFO - Background TTL sweeper started (interval=300s)
ixnetwork-mcp-server  | 2026-10-22 17:11:18,162 - ixnetwork-mcp - INFO - Session registry sweeper started (interval=120s, grace=300s, ttl=86400s)
ixnetwork-mcp-server  | [10/22/26 17:11:18] INFO     Starting MCP server                transport.py:363
ixnetwork-mcp-server  |                              'IxNetwork-MCP' with transport                     
ixnetwork-mcp-server  |                              'sse' on http://0.0.0.0:8000/sse                   
ixnetwork-mcp-server  | INFO:     Started server process [20]
ixnetwork-mcp-server  | INFO:     Waiting for application startup.
ixnetwork-mcp-server  | INFO:     Application startup complete.
ixnetwork-mcp-server  | INFO:     Uvicorn running on https://0.0.0.0:8000 (Press CTRL+C to quit)
ixnetwork-mcp-server  | TLS context loaded and server listening — deleting ephemeral cert/key from /run/ixnetwork-mcp/certs
ixnetwork-mcp-server  | INFO:     127.0.0.1:57430 - "GET /health HTTP/1.1" 200 OK
Gracefully Stopping... press Ctrl+C again to force
Container ixnetwork-mcp-server Stopping 
Container ixnetwork-mcp-server Stopped 
ixnetwork-mcp-server exited with code 143
(.venv) ixnetwork-mcp-server-docker-compose$ docker compose down
[+] down 2/2
 ✔ Container ixnetwork-mcp-server                      Removed                                                                                                0.0s
 ✔ Network ixnetwork-mcp-server-docker-compose_default Removed                                                                                                0.2s
(.venv) ixnetwork-mcp-server-docker-compose$ docker compose up -d
[+] up 2/2
 ✔ Network ixnetwork-mcp-server-docker-compose_default Created                                                                                                0.0s
 ✔ Container ixnetwork-mcp-server                      Started                                                                                                0.2s
(.venv) ixnetwork-mcp-server-docker-compose$ 
```