# cookiecutter-ixnetwork-mcpserver
cookiecutter template for IxNetwork MCP Server

## How to 

```
$ mkdir mcptest
$ cd mcptest
$ uv venv .venv
Using CPython 3.9.21 interpreter at: /bin/python
Creating virtual environment at: .venv
Activate with: source .venv/bin/activate
$ source .venv/bin/activate
(.venv) $ uv pip install cookiecutter
Resolved 22 packages in 329ms
Prepared 22 packages in 273ms
Installed 22 packages in 52ms
 + arrow==1.4.0
 + binaryornot==0.4.4
 + certifi==2026.10.19
 + chardet==5.2.0
 + charset-normalizer==3.5.2
 + click==8.1.8
 + cookiecutter==2.6.0
 + idna==3.20
 + jinja2==3.1.6
 + markdown-it-py==3.0.0
 + markupsafe==3.0.4
 + mdurl==0.1.2
 + pygments==2.21.0
 + python-dateutil==3.0.0
 + python-slugify==8.0.4
 + pyyaml==6.0.3
 + requests==2.32.5
 + rich==15.0.0
 + six==1.17.0
 + text-unidecode==1.3
 + tzdata==2026.5
 + urllib3==2.6.3
(.venv) $ cookiecutter https://github.com/daddy-knows-ixNetwork/cookiecutter-ixnetwork-mcpserver
  [1/12] IXNETWORK_MCP_SERVER_IMAGE (ixnetwork-mcp:26.0.0-147): 
  [2/12] IXNETWORK_MCP_HOST_PORT (9966): 
  [3/12] IXNETWORK_MCP_HOST_IP (172.21.191.86): 10.36.158.14
  [4/12] IXNETWORK_MCP_ENABLE_TLS (true): 
  [5/12] IXNETWORK_MCP_LICENSE_SERVER (10.36.159.38): 
  [6/12] PUBLIC_BASE_URL (https://10.36.158.14:9966): 
  [7/12] IXN_USERNAME (admin): 
  [8/12] IXN_PASSWORD (admin): 
  [9/12] project_name (ixNetwork MCP Server Docker Compose): mcp at 10.36.158.14
  [10/12] project_slug (mcp-at-10_36_158_14): 
  [11/12] project_short_description (A cookiecutter template for IxNetwork MCP Server): 
  [12/12] first_version (0.1.0): 
(.venv) $ ls
mcp-at-10_36_158_14
(.venv) $ cd mcp-at-10_36_158_14/
(.venv) mcp-at-10_36_158_14$ ls
docker-compose.yaml
(.venv) mcp-at-10_36_158_14$ docker compose up
[+] Running 4/4
 ✔ Network mcp-at-10_36_158_14_default              Created                                          0.2s 
 ✔ Volume "mcp-at-10_36_158_14_ixnetwork-mcp-data"  Created                                          0.0s 
 ✔ Volume "mcp-at-10_36_158_14_ixnetwork-mcp-logs"  Created                                          0.0s 
 ✔ Container ixnetwork-mcp-server                   Created                                          0.0s 
Attaching to ixnetwork-mcp-server
ixnetwork-mcp-server  | 2026-10-22 17:33:35,333 - ixnetwork-mcp - INFO - Log file: /var/log/ixnetwork-mcp/ixnetwork-mcp_2026-10-22_173335_20.log
ixnetwork-mcp-server  | 2026-10-22 17:33:35,335 - ixnetwork-mcp - INFO - ixnetwork-mcp version 26.0.0+147
ixnetwork-mcp-server  | 2026-10-22 17:33:35,339 - ixnetwork-mcp - INFO - Licensing configured: 10.36.159.38:7443 [IXN-MCP-BASEx1]
ixnetwork-mcp-server  | 2026-10-22 17:33:35,650 - ixnetwork-mcp - INFO - Licensing initialised against 10.36.159.38:7443 [IXN-MCP-BASEx1]
ixnetwork-mcp-server  | 2026-10-22 17:33:35,650 - ixnetwork-mcp - WARNING - SSE (multi-user) mode enabled. All tool calls require explicit session_id — auto-resolution is disabled.
ixnetwork-mcp-server  | 2026-10-22 17:33:35,650 - ixnetwork-mcp - INFO - PUBLIC_BASE_URL set to https://10.36.158.14:9966
ixnetwork-mcp-server  | 2026-10-22 17:33:35,651 - ixnetwork-mcp - INFO - sse_hooks: installed SSE disconnect hook on SseServerTransport.connect_sse
ixnetwork-mcp-server  | 2026-10-22 17:33:35,651 - ixnetwork-mcp - INFO - Starting IxNetwork MCP Server (transport=sse)
ixnetwork-mcp-server  | 2026-10-22 17:33:35,651 - ixnetwork-mcp - INFO - TLS enabled (ssl_certfile=/run/ixnetwork-mcp/certs/server-98db9690fe5ad8f9.crt)
ixnetwork-mcp-server  | 2026-10-22 17:33:35,652 - ixnetwork-mcp - INFO - SSE server listening on 0.0.0.0:8000
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
ixnetwork-mcp-server  | 2026-10-22 17:33:35,785 - ixnetwork-mcp - INFO - Background TTL sweeper started (interval=300s)
ixnetwork-mcp-server  | 2026-10-22 17:33:35,785 - ixnetwork-mcp - INFO - Session registry sweeper started (interval=120s, grace=300s, ttl=86400s)
ixnetwork-mcp-server  | [10/22/26 17:33:35] INFO     Starting MCP server                transport.py:363
ixnetwork-mcp-server  |                              'IxNetwork-MCP' with transport                     
ixnetwork-mcp-server  |                              'sse' on http://0.0.0.0:8000/sse                   
ixnetwork-mcp-server  | INFO:     Started server process [20]
ixnetwork-mcp-server  | INFO:     Waiting for application startup.
ixnetwork-mcp-server  | INFO:     Application startup complete.
ixnetwork-mcp-server  | INFO:     Uvicorn running on https://0.0.0.0:8000 (Press CTRL+C to quit)
ixnetwork-mcp-server  | TLS context loaded and server listening — deleting ephemeral cert/key from /run/ixnetwork-mcp/certs
ixnetwork-mcp-server  | INFO:     127.0.0.1:46936 - "GET /health HTTP/1.1" 200 OK
Gracefully stopping... (press Ctrl+C again to force)
[+] Stopping 1/1
 ✔ Container ixnetwork-mcp-server  Stopped                                                           0.2s 
(.venv) mcp-at-10_36_158_14$ docker compose down
[+] Running 2/2
 ✔ Container ixnetwork-mcp-server       Removed                                                      0.0s 
 ✔ Network mcp-at-10_36_158_14_default  Removed                                                      0.4s 
(.venv) mcp-at-10_36_158_14$ docker compose up -d
[+] Running 2/2
 ✔ Network mcp-at-10_36_158_14_default  Created                                                      0.2s 
 ✔ Container ixnetwork-mcp-server       Started                                                      0.3s 
(.venv) mcp-at-10_36_158_14$
```