# 🚀 AI LaunchKit

<div align="center">

**Open-Source AI Development Toolkit**

*Deploy your complete AI stack in minutes, not weeks*

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/freddy-schuetz/ai-launchkit?style=social)](https://github.com/freddy-schuetz/ai-launchkit)
[![Based on](https://img.shields.io/badge/Based%20on-n8n--installer-green)](https://github.com/kossakovsky/n8n-installer)

[Installation](#-installation) • [Features](#-whats-included) • [Documentation](#-documentation) • [Support](#-support)

</div>

---

## 🎯 What is AI LaunchKit?

AI LaunchKit is a comprehensive, self-hosted AI development environment that deploys **50+ pre-configured tools** with a single command. Build AI applications, automate workflows, generate images, and develop with AI assistance - all running on your own infrastructure.

Originally forked from [n8n-installer](https://github.com/kossakovsky/n8n-installer), AI LaunchKit has evolved into a complete AI development platform, maintained by [Friedemann Schuetz](https://www.linkedin.com/in/friedemann-schuetz).

### 🎬 Quick Demo

```bash
# One command to rule them all
git clone https://github.com/freddy-schuetz/ai-launchkit && cd ai-launchkit && sudo bash ./scripts/install.sh
```

**That's it!** Your AI development stack is ready in ~10-15 minutes.

**ATTENTION!** The AI LaunchKit is currently in development. It is regularly tested and updated. However, use is at your own risk!

---

## ✨ What's Included

### 📧 Mail System

| Tool | Description | Always Active | Purpose |
|------|-------------|---------------|----------|
| **[Mailpit](https://github.com/axllent/mailpit)** | Mail catcher with web UI Access: `mail.yourdomain.com` | ✅ Yes | Development/Testing - captures all emails |
| **[Docker-Mailserver](https://github.com/docker-mailserver/docker-mailserver)** | Production mail server | ⚡ Optional | Real email delivery for production |
| **[SnappyMail](https://github.com/the-djmaze/snappymail)** | Modern webmail client Access: `webmail.yourdomain.com` | ⚡ Optional | Web interface for Docker-Mailserver |

**Mail Configuration:**
- Mailpit automatically configured for all services (always active)
- Docker-Mailserver available for production email delivery (optional)
- SnappyMail provides a modern web interface for email access (optional, requires Docker-Mailserver)
- Web UI to view all captured emails
- Zero manual configuration needed!

### 🔧 Workflow Automation

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[n8n](https://github.com/n8n-io/n8n)** | Visual workflow automation platform | API integrations, data pipelines, business automation | `n8n.yourdomain.com` |
| **[n8n-MCP](https://github.com/czlonkowski/n8n-mcp)** | AI workflow generator for n8n | Claude/Cursor integration, 525+ node docs, workflow validation | `n8nmcp.yourdomain.com` |
| **300+ Workflows** | Pre-built n8n templates | Email automation, social media, data sync, AI workflows | Imported on install |

### 🎯 User Interfaces

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Open WebUI](https://github.com/open-webui/open-webui)** | ChatGPT-like interface for LLMs | AI chat, model switching, conversation management | `webui.yourdomain.com` |
| **[Postiz](https://github.com/gitroomhq/postiz-app)** | Social media management platform | Content scheduling, analytics, multi-platform posting | `postiz.yourdomain.com` |

### 📹 Video Conferencing

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Jitsi Meet](https://github.com/jitsi/jitsi-meet)** ⚠️ | Professional video conferencing platform | Client meetings, team calls, webinars, Cal.com integration | `meet.yourdomain.com` |

**⚠️ Jitsi Meet Requirements:**
- **CRITICAL:** Requires UDP Port 10000 for WebRTC audio/video
- Many VPS providers block UDP traffic by default
- Without UDP 10000: Only chat works, no audio/video!
- Test UDP connectivity before production use
- Alternative: Use external services (Zoom, Google Meet) with Cal.com

### 💼 Business & Productivity

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Cal.com](https://github.com/calcom/cal.com)** | Open-source scheduling platform | Meeting bookings, team calendars, payment integrations | `cal.yourdomain.com` |
| **[Vikunja](https://github.com/go-vikunja/vikunja)** | Modern task management platform | Kanban boards, Gantt charts, team collaboration, CalDAV | `vikunja.yourdomain.com` |
| **[Leantime](https://github.com/Leantime/leantime)** | Goal-oriented project management suite | ADHD-friendly PM, time tracking, sprints, strategy tools | `leantime.yourdomain.com` |
| **[Kimai](https://github.com/kimai/kimai)** | Professional time tracking | DSGVO-compliant billing, team timesheets, API, 2FA, invoicing | `time.yourdomain.com` |
| **[Invoice Ninja](https://github.com/invoiceninja/invoiceninja)** | Professional invoicing & payment platform | Multi-currency invoices, 40+ payment gateways, recurring billing, client portal | `invoices.yourdomain.com` |
| **[Baserow](https://github.com/bram2w/baserow)** | Airtable Alternative with real-time collaboration | Database management, project tracking, collaborative workflows | `baserow.yourdomain.com` |
| **[NocoDB](https://github.com/nocodb/nocodb)** | Open-source Airtable alternative with API & webhooks | Smart spreadsheet UI, realtime collaboration, automation | `nocodb.yourdomain.com` |
| **[Formbricks](https://github.com/formbricks/formbricks)** | Privacy-first survey platform | Customer feedback, NPS surveys, market research, form builder, GDPR-compliant | `forms.yourdomain.com` |
| **[Metabase](https://github.com/metabase/metabase)** | User-friendly business intelligence platform | No-code dashboards, automated reports, data exploration, team analytics | `analytics.yourdomain.com` |
| **[Odoo 18](https://github.com/odoo/odoo)** | Open Source ERP/CRM with AI features | Sales automation, inventory, accounting, AI lead scoring | `odoo.yourdomain.com` |
| **[Twenty CRM](https://github.com/twentyhq/twenty)** | Modern Notion-like CRM | Customer pipelines, GraphQL API, team collaboration, lightweight CRM for startups | `twenty.yourdomain.com` |
| **[EspoCRM](https://github.com/espocrm/espocrm)** | Full-featured CRM platform | Email campaigns, workflow automation, advanced reporting, role-based access | `espocrm.yourdomain.com` |
| **[Mautic](https://github.com/mautic/mautic)** | Marketing automation platform | Lead scoring, email campaigns, landing pages, multi-channel marketing, automation workflows | `mautic.yourdomain.com` |

### 🎨 AI Content Generation

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[ComfyUI](https://github.com/comfyanonymous/ComfyUI)** | Node-based Stable Diffusion interface | Image generation, AI art, photo editing, workflows | `comfyui.yourdomain.com` |

### 💻 AI-Powered Development / Vibe Coding

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[bolt.diy](https://github.com/stackblitz-labs/bolt.diy)** | Build full-stack apps with prompts | Rapid prototyping, MVP creation, learning to code | `bolt.yourdomain.com` |
| **[OpenUI](https://github.com/wandb/openui)** 🧪 | AI-powered UI component generation | Design systems, component libraries, mockups | `openui.yourdomain.com` |

### 🤖 AI Agents

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Flowise](https://github.com/FlowiseAI/Flowise)** | Visual AI agent builder | Chatbots, customer support, AI workflows | `flowise.yourdomain.com` |
| **[LiveKit](https://github.com/livekit/livekit)** + Agents | Real-time voice agents with WebRTC (auto-uses Whisper/TTS/Ollama or OpenAI) | AI voice assistants, conversational AI, ChatGPT-like voice bots, requires UDP 50000-50100 | `livekit.yourdomain.com` |
| **[Dify](https://github.com/langgenius/dify)** | LLMOps platform for AI apps | Production AI apps, model management, prompt engineering | `dify.yourdomain.com` |
| **[Letta](https://github.com/letta-ai/letta)** | Stateful agent server | Persistent AI assistants, memory management | `letta.yourdomain.com` |
| **[Browser-use](https://github.com/browser-use/browser-use)** | LLM-powered browser control | Web scraping, form filling, automated testing | Internal API only |
| **[Skyvern](https://skyvern.com)** | Vision-based browser automation | Complex web tasks, CAPTCHA handling, dynamic sites | Internal API only |
| **[Browserless](https://browserless.io)** | Headless Chrome service | Puppeteer/Playwright hub, PDF generation, screenshots | Internal WebSocket |

### 📚 RAG Systems

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[RAGApp](https://github.com/ragapp/ragapp)** | Build RAG assistants over your data | Knowledge bases, document Q&A, research tools | `ragapp.yourdomain.com` |
| **[Qdrant](https://github.com/qdrant/qdrant)** | High-performance vector database | Semantic search, recommendations, RAG storage | `qdrant.yourdomain.com` |
| **[Weaviate](https://github.com/weaviate/weaviate)** | AI-native vector database | Hybrid search, multi-modal data, GraphQL API | `weaviate.yourdomain.com` |

### 🎙️ Speech, Language & Text Processing

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Faster-Whisper](https://github.com/SYSTRAN/faster-whisper)** | OpenAI-compatible Speech-to-Text | Transcription, voice commands, meeting notes | Internal API |
| **[OpenedAI-Speech](https://github.com/matatonic/openedai-speech)** | OpenAI-compatible Text-to-Speech | Voice assistants, audiobooks, notifications | Internal API |
| **[TTS Chatterbox](https://github.com/resemble-ai/chatterbox)** | State-of-the-art TTS with emotion control & voice cloning | AI voices with emotional expression, voice synthesis, outperforms ElevenLabs | `chatterbox.yourdomain.com` |
| **[LibreTranslate](https://github.com/LibreTranslate/LibreTranslate)** | Self-hosted translation API | 50+ languages, document translation, privacy-focused | `translate.yourdomain.com` |
| **OCR Bundle: [Tesseract](https://github.com/tesseract-ocr/tesseract) & [EasyOCR](https://github.com/JaidedAI/EasyOCR)** | Dual OCR engines: Tesseract (fast) + EasyOCR (quality) | Text extraction from images/PDFs, receipt scanning, document digitization | Internal API |
| **[Scriberr](https://github.com/rishikanthc/Scriberr)** | AI audio transcription with WhisperX & speaker diarization | Meeting transcripts, podcast processing, call recordings, speaker identification | `scriberr.yourdomain.com` |
| **[Vexa](https://github.com/Vexa-ai/vexa)** | Real-time meeting transcription API | Live transcription for Google Meet & Teams, speaker identification, 99 languages, n8n integration | Internal API |

*If you have troubles installing or updating Vexa, please view this guide:* **[Vexa Workaround](https://github.com/freddy-schuetz/ai-launchkit/blob/main/vexa-troubleshooting-workarounds.md)**

### 🔍 Search & Web Data

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[SearXNG](https://github.com/searxng/searxng)** | Privacy-respecting metasearch engine | Web search for agents, no tracking, multiple sources | `searxng.yourdomain.com` |
| **[Perplexica](https://github.com/ItzCrazyKns/Perplexica)** | Open-source AI-powered search engine | Deep research, academic search, Perplexity AI alternative | `perplexica.yourdomain.com` |
| **[Crawl4Ai](https://github.com/unclecode/crawl4ai)** | AI-optimized web crawler | Web scraping, data extraction, site monitoring | Internal API |
| **[GPT Researcher](https://github.com/assafelovic/gpt-researcher)** | Autonomous research agent (2000+ word reports) | Comprehensive research reports, multi-source analysis, citations | `research.yourdomain.com` |
| **[Local Deep Research](https://github.com/langchain-ai/local-deep-researcher)** | LangChain's iterative deep research (~95% accuracy) | Fact-checking, detailed analysis, research loops with reflection | Internal API |

### 🧠 Knowledge Graphs

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Neo4j](https://github.com/neo4j/neo4j)** | Graph database platform | Knowledge graphs, entity relationships, fraud detection, recommendations | `neo4j.yourdomain.com` |
| **[LightRAG](https://github.com/HKUDS/LightRAG)** | Graph-based RAG with entity extraction | Automatic knowledge graph creation, relationship mapping, complex queries | `lightrag.yourdomain.com` |

### 🎬 Media Processing Suite

Pre-installed in the n8n container for seamless media manipulation:

| Tool | Description | Use Cases |
|------|-------------|-----------|
| **[FFmpeg](https://github.com/FFmpeg/FFmpeg)** | Industry-standard multimedia framework | Video conversion, streaming, audio extraction |
| **[ImageMagick](https://github.com/ImageMagick/ImageMagick)** | Image manipulation toolkit | Format conversion, resizing, effects, thumbnails |
| **[ExifTool](https://github.com/exiftool/exiftool)** | Metadata management | Read/write EXIF, IPTC, XMP metadata |
| **[MediaInfo](https://github.com/MediaArea/MediaInfo)** | Media file analyzer | Codec detection, bitrate analysis, format info |
| **[SoX](http://sox.sourceforge.net/)** | Sound processing utility | Audio format conversion, effects, resampling |
| **[Ghostscript](https://github.com/ArtifexSoftware/ghostscript)** | PDF/PostScript processor | PDF manipulation, conversion, optimization |
| **Python3 + Libraries** | Pillow, OpenCV, NumPy, Pandas | Image processing, data analysis, automation |

### 🗄️ Data Infrastructure

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Supabase](https://github.com/supabase/supabase)** | Open-source Firebase alternative | Instant APIs, auth, realtime, storage, edge functions | `supabase.yourdomain.com` |
| **[PostgreSQL 17](https://www.postgresql.org/)** | Advanced relational database | Primary database for n8n, Cal.com, and other services | Internal only |
| **[Redis](https://github.com/redis/redis)** | In-memory data store | Queue management, caching, session storage | Internal only |

### ⚙️ System Management

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** | Bitwarden-compatible password manager | Credential management, team password sharing, auto-fill | `vault.yourdomain.com` |
| **[Caddy](https://github.com/caddyserver/caddy)** | Automatic HTTPS reverse proxy | SSL certificates, load balancing, routing | Automatic |
| **[Cloudflare Tunnel](https://github.com/cloudflare/cloudflared)** | Secure tunnel without port forwarding | Zero-trust access, DDoS protection, firewall bypass | Optional |
| **[Python Runner](https://github.com/n8n-io/n8n)** | Isolated Python environment | Execute Python scripts from n8n workflows | Internal only |
| **[Grafana](https://github.com/grafana/grafana)** | Metrics visualization platform | System monitoring, performance dashboards, alerting | `grafana.yourdomain.com` |
| **[Prometheus](https://github.com/prometheus/prometheus)** | Metrics collection & alerting | Time-series database, service monitoring, resource tracking | Internal only |
| **[Portainer](https://github.com/portainer/portainer)** | Docker management interface | Container monitoring, logs, restart services | `portainer.yourdomain.com` |

### 🧰 AI Support Tools

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[Ollama](https://github.com/ollama/ollama)** | Local LLM runtime | Run Llama, Mistral, Phi locally, API-compatible | `ollama.yourdomain.com` |
| **[Gotenberg](https://github.com/gotenberg/gotenberg)** | Universal document converter | HTML/Markdown → PDF, Office → PDF, merge PDFs | Internal API |
| **[Stirling-PDF](https://github.com/Stirling-Tools/Stirling-PDF)** | PDF toolkit | Split, merge, compress, OCR, sign PDFs | `pdf.yourdomain.com` |

### 🛡️ AI Security & Compliance

| Tool | Description | Use Cases | Access |
|------|-------------|-----------|--------|
| **[LLM Guard](https://github.com/protectai/llm-guard)** | Input/output filtering for LLMs | Prompt injection prevention, toxicity filtering, PII removal | Internal API |
| **[Microsoft Presidio](https://github.com/microsoft/presidio)** | PII detection & anonymization (English) | GDPR compliance, data protection, sensitive data handling | Internal API |
| **[Flair NER](https://github.com/flairNLP/flair)** | German PII detection | DSGVO compliance, German text processing, entity recognition | Internal API |

---

## 🚀 Quick Start

### Installation Command

```bash
git clone https://github.com/freddy-schuetz/ai-launchkit && cd ai-launchkit && sudo bash ./scripts/install.sh
```

### What the Installer Does

1. **Checks Prerequisites** - Verifies Docker, domain, and system requirements
2. **Configures Services** - Sets up environment variables and generates secure passwords
3. **Deploys Stack** - Starts all selected services with Docker Compose
4. **Obtains SSL Certificates** - Automatic HTTPS via Caddy
5. **Imports Workflows** - Optional: Downloads 300+ pre-built n8n templates
6. **Generates Report** - Provides access URLs and credentials

### After Installation

1. **Access n8n:** Navigate to `https://n8n.yourdomain.com`
2. **Create Admin Account:** First visitor becomes owner
3. **Configure API Keys:** Add OpenAI, Anthropic, Groq keys in `.env` file
4. **Explore Services:** Check the final report for all URLs and credentials
5. **Import Credentials to Vaultwarden:** Run `sudo bash ./scripts/download_credentials.sh`

### Installation Time

- **Base Installation:** 10-15 minutes
- **With Workflow Import:** +20-30 minutes (optional)
- **Total:** 15-45 minutes depending on selections

**System Requirements:**
- 4GB RAM minimum (8GB+ recommended)
- 40GB disk space (more for media/models)
- Ubuntu 22.04/24.04 or Debian 11/12
- Domain with wildcard DNS configured

---

## 📦 Installation - Detailliert

### Prerequisites

Before installing AI LaunchKit, ensure you have:

1. **Server:** Ubuntu 22.04/24.04 or Debian 11/12 LTS
   - 4GB RAM minimum (8GB+ recommended for AI workloads)
   - 40GB+ disk space (SSD recommended)
   - Root or sudo access

2. **Domain:** A registered domain with wildcard DNS
   ```
   A *.yourdomain.com -> YOUR_SERVER_IP
   ```

3. **Access:** SSH access to your server

### Step-by-Step Installation

#### Step 1: Connect to Your Server

```bash
# Connect via SSH
ssh root@YOUR_SERVER_IP

# Or with key authentication
ssh -i ~/.ssh/your-key.pem user@YOUR_SERVER_IP
```

#### Step 2: Clone Repository

```bash
# Clone AI LaunchKit
git clone https://github.com/freddy-schuetz/ai-launchkit

# Navigate into directory
cd ai-launchkit
```

#### Step 3: Run Installer

```bash
# Start installation wizard
sudo bash ./scripts/install.sh
```

#### Step 4: Answer Installation Prompts

The installer will ask you for:

**1. Domain Name:**
```
Enter your domain (e.g., example.com): yourdomain.com
```

**2. Email Address:**
```
Enter email for SSL certificates: admin@yourdomain.com
```

**3. API Keys (Optional):**
```
Enter OpenAI API key (or press Enter to skip): sk-...
Enter Anthropic API key (or press Enter to skip): sk-ant-...
Enter Groq API key (or press Enter to skip): gsk_...
```

**4. Community Workflows (Optional):**
```
Import 300+ n8n community workflows? [y/N]: y
```
*Note: This takes 20-30 minutes extra*

**5. Worker Configuration:**
```
How many n8n workers? (1-4): 2
```

**6. Service Selection:**
```
Install Docker-Mailserver for production email? [y/N]: n
Install SnappyMail webmail client? [y/N]: n
Install Jitsi Meet? [y/N]: y
... (and more services)
```

#### Step 5: Installation Progress

The installer will now:
1. ✅ Install Docker and Docker Compose
2. ✅ Generate secure passwords
3. ✅ Configure services
4. ✅ Start Docker containers
5. ✅ Request SSL certificates
6. ✅ Import workflows (if selected)
7. ✅ Generate final report

#### Step 6: Save Installation Report

At the end, you'll see:

```
================================
Installation Complete! 🎉
================================

Access URLs:
  n8n: https://n8n.yourdomain.com
  bolt.diy: https://bolt.yourdomain.com
  Mailpit: https://mail.yourdomain.com
  ... (more services)

Download credentials with:
sudo bash ./scripts/download_credentials.sh
```

**Important:** Save the installation output - it contains all passwords!

### Post-Installation Steps

#### First Login to Services

**n8n (Workflow Automation):**
1. Open `https://n8n.yourdomain.com`
2. First visitor creates owner account
3. Choose strong password (min 8 characters)
4. Setup complete!

**Vaultwarden (Password Manager):**
1. Open `https://vault.yourdomain.com`
2. Click "Create Account"
3. Set master password (very strong!)
4. Import AI LaunchKit credentials:
   ```bash
   sudo bash ./scripts/download_credentials.sh
   ```
5. Download JSON file and import in Vaultwarden

**Other Services:**
- Most services: First user = admin
- Some require credentials from `.env` file
- Check the installation output or `.env` file for credentials

#### Configure API Keys (Optional)

If you skipped API keys during installation:

```bash
# Edit environment file
nano .env

# Add your keys:
OPENAI_API_KEY=sk-your-key-here
ANTHROPIC_API_KEY=sk-ant-your-key-here
GROQ_API_KEY=gsk_your-key-here

# Save and exit (Ctrl+X, Y, Enter)

# Apply changes
docker compose restart
```

#### DNS Verification

Ensure your domains are resolving correctly:

```bash
# Test DNS resolution
nslookup n8n.yourdomain.com
nslookup bolt.yourdomain.com

# Test HTTPS access
curl -I https://n8n.yourdomain.com
# Should return: HTTP/2 200
```

#### Firewall Check

Verify firewall rules are correct:

```bash
sudo ufw status

# Should show:
# 22/tcp                     ALLOW       Anywhere
# 80/tcp                     ALLOW       Anywhere
# 443/tcp                    ALLOW       Anywhere
```

### Optional: Docker-Mailserver Setup

If you selected Docker-Mailserver for production email:

#### Add Email Accounts

```bash
# Create first email account
docker exec -it mailserver setup email add admin@yourdomain.com

# Create additional accounts
docker exec -it mailserver setup email add noreply@yourdomain.com
docker exec -it mailserver setup email add support@yourdomain.com

# List all accounts
docker exec mailserver setup email list
```

#### Configure DNS for Email

**Required DNS Records:**

```
# MX Record
Type: MX
Name: @
Value: mail.yourdomain.com
Priority: 10

# A Record for mail
Type: A  
Name: mail
Value: YOUR_SERVER_IP

# SPF Record
Type: TXT
Name: @
Value: v=spf1 mx ~all

# DMARC Record
Type: TXT
Name: _dmarc
Value: v=DMARC1; p=none; rua=mailto:postmaster@yourdomain.com
```

#### Generate DKIM Keys

```bash
# Generate DKIM signature
docker exec mailserver setup config dkim

# Get public key for DNS
docker exec mailserver cat /tmp/docker-mailserver/opendkim/keys/yourdomain.com/mail.txt

# Add as TXT record:
# Name: mail._domainkey
# Value: (paste the key from above)
```

### Troubleshooting Installation

#### Services Won't Start

```bash
# Check Docker is running
sudo systemctl status docker

# Check specific service logs
docker compose logs [service-name] --tail 50

# Common issues:
# - Not enough RAM: Reduce services or upgrade server
# - Port conflicts: Check if ports 80/443 are free
# - DNS not ready: Wait 15 minutes for propagation
```

#### SSL Certificate Errors

```bash
# Caddy might take a few minutes to get certificates
# Check Caddy logs:
docker compose logs caddy --tail 50

# If problems persist:
# 1. Verify DNS is correct
# 2. Check firewall allows 80/443
# 3. Restart Caddy
docker compose restart caddy
```

#### Docker Issues

```bash
# Restart Docker daemon
sudo systemctl restart docker

# Reset Docker network (if needed)
docker network prune -f

# Restart all services
cd ai-launchkit
docker compose restart
```

---

## 🔄 Update - Detailliert

### When to Update

Update AI LaunchKit when:
- New features are released
- Security patches are available
- Bug fixes are published
- You want the latest service versions

**Check for updates:**
```bash
cd ai-launchkit
git fetch origin
git log HEAD..origin/main --oneline
```

### Backup Before Update

**CRITICAL:** Always backup before updating!

```bash
# Navigate to AI LaunchKit
cd ai-launchkit

# Backup all Docker volumes
tar czf backup-$(date +%Y%m%d).tar.gz \
  /var/lib/docker/volumes/localai_*

# Backup PostgreSQL database
docker exec postgres pg_dumpall -U postgres > backup-$(date +%Y%m%d).sql

# Backup .env file
cp .env .env.backup

# Backup Docker Compose
cp docker-compose.yml docker-compose.yml.backup
```

**Move backups to safe location:**
```bash
# Create backup directory
mkdir -p ~/ai-launchkit-backups

# Move backups
mv backup-*.tar.gz ~/ai-launchkit-backups/
mv backup-*.sql ~/ai-launchkit-backups/

# Verify backups exist
ls -lh ~/ai-launchkit-backups/
```

### Update Procedure

#### Standard Update Process

```bash
# 1. Navigate to AI LaunchKit
cd ai-launchkit

# 2. Stop all services gracefully
docker compose down

# 3. Backup (see section above)
# ... (perform backups)

# 4. Pull latest changes
git pull

# 5. Pull new Docker images
docker compose pull

# 6. Start services with new images
docker compose up -d

# 7. Check service status
docker compose ps

# 8. Monitor logs for issues
docker compose logs -f --tail 100
```

#### Update with Service Changes

If the update adds new services or changes configuration:

```bash
# 1. Stop services
docker compose down

# 2. Backup everything
# ... (perform backups)

# 3. Pull latest code
git pull

# 4. Review .env.example for new variables
diff .env .env.example

# 5. Add new variables to .env
nano .env
# Add any new required variables

# 6. Pull new images
docker compose pull

# 7. Recreate services with new config
docker compose up -d --force-recreate

# 8. Verify all services started
docker compose ps
```

### PostgreSQL Version Handling

**Important:** AI LaunchKit pins PostgreSQL to version 17 to prevent automatic upgrades.

#### Check Current PostgreSQL Version

```bash
docker exec postgres postgres --version
```

#### If You Have PostgreSQL 18

If you installed after September 26, 2025 and have PostgreSQL 18:

```bash
# Pin to PostgreSQL 18 in .env
echo "POSTGRES_VERSION=18" >> .env

# Update safely
bash scripts/update.sh
```

#### If You Experience Database Errors

If you see "database files are incompatible" errors:

<details>
<summary><b>Emergency Recovery Steps</b></summary>

```bash
# 1. BACKUP YOUR DATA (CRITICAL!)
docker exec postgres pg_dumpall -U postgres > emergency-backup.sql

# 2. Stop all services
docker compose down

# 3. Remove incompatible volume
docker volume rm localai_postgres_data

# 4. Pull latest fixes
git pull

# 5. Start PostgreSQL (now pinned to v17)
docker compose up -d postgres
sleep 10

# 6. Restore your data
docker exec -i postgres psql -U postgres < emergency-backup.sql

# 7. Start all services
docker compose up -d
```

</details>

#### Version Verification

After update, verify versions:

```bash
docker exec postgres postgres --version
# Should show: PostgreSQL 17.x or 18.x (if pinned)
```

### Post-Update Verification

#### Check Service Status

```bash
# View all services
docker compose ps

# All should show: STATUS = Up
# If any show "Restarting" wait 2-3 minutes, then check logs:
docker compose logs [service-name] --tail 50
```

#### Test Key Services

**n8n:**
```bash
curl -I https://n8n.yourdomain.com
# Should return: HTTP/2 200
```

**Database:**
```bash
docker exec postgres pg_isready -U postgres
# Should return: accepting connections
```

**Redis:**
```bash
docker exec redis redis-cli ping
# Should return: PONG
```

#### Monitor Resource Usage

```bash
# Check memory and CPU
docker stats --no-stream

# Check disk space
df -h
```

#### Verify Workflows Still Run

1. Open n8n: `https://n8n.yourdomain.com`
2. Open a test workflow
3. Click "Execute Workflow"
4. Verify it completes successfully

### Rollback Procedure

If the update causes issues, rollback to the previous version:

#### Quick Rollback

```bash
# 1. Navigate to AI LaunchKit
cd ai-launchkit

# 2. View commit history
git log --oneline -10

# 3. Rollback to previous commit
git reset --hard [previous-commit-hash]

# 4. Restore .env if needed
cp .env.backup .env

# 5. Restart with old version
docker compose down
docker compose up -d
```

#### Full Rollback with Data Restore

```bash
# 1. Stop services
docker compose down

# 2. Restore volumes from backup
tar xzf volumes-backup-YYYYMMDD.tar.gz

# 3. Restore PostgreSQL
docker compose up -d postgres
sleep 10
docker exec -i postgres psql -U postgres < backup-YYYYMMDD.sql

# 4. Start all services
docker compose up -d
```

### Service-Specific Updates

Some services may require additional steps:

#### ComfyUI Models

```bash
# Models are not automatically updated
# To update models, manually download new versions to:
/var/lib/docker/volumes/localai_comfyui_data/_data/models/
```

#### Ollama Models

```bash
# Update installed models
docker exec ollama ollama pull llama3.2
docker exec ollama ollama pull mistral
```

#### n8n Community Nodes

```bash
# Update community nodes
docker exec n8n npm update -g n8n

# Restart n8n
docker compose restart n8n
```

#### Supabase

```bash
# Supabase has multiple components
# All update together with docker compose pull
docker compose pull supabase-kong supabase-auth supabase-rest supabase-storage
docker compose up -d supabase-kong supabase-auth supabase-rest supabase-storage
```

### Update Troubleshooting

#### Services Won't Start After Update

```bash
# Check logs for specific error
docker compose logs [service-name] --tail 100

# Common fixes:
# 1. Recreate service
docker compose up -d --force-recreate [service-name]

# 2. Clear cache and restart
docker compose down
docker system prune -f
docker compose up -d

# 3. Restore from backup if needed
```

#### Database Connection Errors

```bash
# PostgreSQL not starting
docker compose logs postgres --tail 100

# Common causes:
# - Incompatible data format (see PostgreSQL section)
# - Corrupted data (restore from backup)
# - Insufficient disk space (check with df -h)
```

#### Port Conflicts After Update

```bash
# Check what's using the port
sudo lsof -i :80
sudo lsof -i :443

# Stop conflicting service
sudo systemctl stop [service-name]

# Or change port in .env
nano .env
# Change PORT_VARIABLE to different port
```

#### Missing Environment Variables

```bash
# Compare with .env.example
diff .env .env.example

# Add any missing variables
nano .env

# Restart services
docker compose restart
```

### Maintenance Updates

#### Regular Maintenance

```bash
# Clean up old Docker resources (monthly)
docker system prune -af --volumes

# Update system packages (monthly)
sudo apt update && sudo apt upgrade -y

# Check disk space (weekly)
df -h
docker system df
```

#### Security Updates

```bash
# Update OS security patches
sudo apt update
sudo apt upgrade -y

# Update Docker
sudo apt install docker-ce docker-ce-cli containerd.io

# Restart Docker daemon
sudo systemctl restart docker

# Restart all services
docker compose restart
```

### Update Best Practices

1. **Always Backup First** - Cannot stress this enough
2. **Test in Staging** - If you have a test environment
3. **Read Changelogs** - Know what's changing
4. **Update Off-Peak** - Minimize user impact
5. **Monitor After Update** - Watch logs for 24 hours
6. **Keep Backups** - Retain last 3-5 backups
7. **Document Changes** - Note what was updated and when

### Update Notifications

Stay informed about updates:

- **Watch GitHub Repository**: Get notifications for new releases
- **Join Community Forum**: [oTTomator Think Tank](https://thinktank.ottomator.ai/c/local-ai/18)
- **Discord** *(coming soon)*: Real-time update announcements

### Getting Help with Updates

If you encounter issues:

1. **Check Logs**: `docker compose logs [service]`
2. **Search Issues**: [GitHub Issues](https://github.com/freddy-schuetz/ai-launchkit/issues)
3. **Community Forum**: Ask for help
4. **Rollback**: Use the procedure above if needed

---

**Next Steps:** After updating, explore the [Services section](#-services) for new features in each tool.

---

## 📧 Services

This section provides detailed information for each service, including setup, n8n integration examples, and troubleshooting.

<!-- Each service will be added as an expandable <details> section in Phase 2 -->

### Mail System

<details>
<summary><b>📧 Mailpit - Development Mail Catcher</b></summary>

### What is Mailpit?

Mailpit is a modern email testing server with an integrated web UI. It captures all outgoing emails and displays them in a user-friendly interface - perfect for development and testing.

### Features

- **Email Capture:** Catches ALL emails from all services
- **Web UI:** Modern, fast, responsive interface
- **Real-time Updates:** New emails appear instantly
- **Search & Filter:** Search emails by sender, subject, etc.
- **API Access:** Programmatic access to emails
- **Zero Configuration:** Works out-of-the-box

### Initial Setup

**Mailpit is already pre-configured!** No setup required.

**Access the Web UI:**

1. Navigate to `https://mail.yourdomain.com`
2. No authentication required
3. All emails sent by services appear automatically here

**All services are pre-configured:**
- SMTP Host: `mailpit`
- SMTP Port: `1025`
- No authentication required
- No SSL/TLS

### n8n Integration Setup

Mailpit is **already pre-configured in n8n**. All "Send Email" nodes use Mailpit automatically.

**Send email from n8n (already configured):**

1. Create workflow
2. Add "Send Email" node
3. Node is already configured with Mailpit
4. Email is automatically captured in Mailpit

**Internal URL for manual configuration:** `http://mailpit:1025`

### Example Workflows

#### Example 1: Send Test Email

```javascript
// 1. Manual Trigger Node

// 2. Send Email Node (already pre-configured)
{
  "to": "test@example.com",
  "subject": "Test from AI LaunchKit",
  "text": "This email was captured by Mailpit!"
}

// 3. Open Mailpit Web UI
// → Email appears instantly at mail.yourdomain.com
```

#### Example 2: Test Automated Notifications

```javascript
// 1. Webhook Trigger Node
// Receives POST from external service

// 2. Code Node - Format email
const emailData = {
  to: "admin@example.com",
  subject: `New Notification: ${$json.event}`,
  html: `
    <h2>Event Details</h2>
    <p><strong>Type:</strong> ${$json.event}</p>
    <p><strong>Time:</strong> ${new Date().toLocaleString()}</p>
    <p><strong>Data:</strong> ${JSON.stringify($json.data, null, 2)}</p>
  `
};
return emailData;

// 3. Send Email Node
// → Sends to Mailpit for review

// 4. Test in Mailpit Web UI
// → Validate HTML formatting and data
```

#### Example 3: Test Service Email Configuration

```javascript
// Test Cal.com, Vikunja, Invoice Ninja, etc.
// All services → Mailpit automatically configured

// Test process:
// 1. Perform action in service (e.g., book meeting in Cal.com)
// 2. Service sends email
// 3. Check email in Mailpit Web UI
// 4. Validate format and content

// No code needed - services send directly to Mailpit!
```

### Troubleshooting

**Emails not appearing in Mailpit:**

```bash
# 1. Check Mailpit status
docker ps | grep mailpit
# Should show: STATUS = Up

# 2. Check Mailpit logs
docker logs mailpit --tail 50

# 3. Test SMTP connection
docker exec n8n nc -zv mailpit 1025
# Should return: Connection successful

# 4. Test from another container
docker exec -it [service-name] sh
nc -zv mailpit 1025
```

**Mailpit Web UI not accessible:**

```bash
# 1. Check Caddy logs
docker logs caddy | grep mailpit

# 2. Restart Mailpit container
docker compose restart mailpit

# 3. Clear browser cache
# CTRL+F5 or incognito mode

# 4. Check DNS
nslookup mail.yourdomain.com
# Should return your server IP
```

**Service cannot send emails:**

```bash
# 1. Check service SMTP settings
docker exec [service] env | grep SMTP
# Should show: SMTP_HOST=mailpit, SMTP_PORT=1025

# 2. Check Docker network
docker network inspect ai-launchkit_default | grep mailpit

# 3. Check service logs
docker logs [service] | grep -i "mail\|smtp"

# 4. Restart service
docker compose restart [service]
```

### Resources

- **GitHub:** https://github.com/axllent/mailpit
- **Documentation:** https://mailpit.axllent.org/docs/
- **API Documentation:** https://mailpit.axllent.org/docs/api/
- **Web-UI:** `https://mail.yourdomain.com`

</details>

<details>
<summary><b>📬 Docker-Mailserver - Production Email</b></summary>

### What is Docker-Mailserver?

Docker-Mailserver is a full-featured, production-ready mail server (SMTP, IMAP) with integrated spam protection and security features. Perfect for real email delivery in production.

### Features

- **Full SMTP/IMAP Support:** Real email delivery and receiving
- **DKIM/SPF/DMARC:** Configured for best deliverability
- **Rspamd Integration:** Automatic spam protection
- **User Management:** Easy CLI tools for account management
- **Secure by Default:** TLS/STARTTLS, modern cipher suites

### Initial Setup

**Prerequisite:** Docker-Mailserver must have been selected during installation.

#### 1. Configure DNS Records

These DNS entries are **required** for email delivery:

**MX Record:**
```
Type: MX
Name: @ (or yourdomain.com)
Value: mail.yourdomain.com
Priority: 10
```

**A Record for mail subdomain:**
```
Type: A
Name: mail
Value: YOUR_SERVER_IP
```

**SPF Record:**
```
Type: TXT
Name: @ (or yourdomain.com)
Value: "v=spf1 mx ~all"
```

**DMARC Record:**
```
Type: TXT
Name: _dmarc
Value: "v=DMARC1; p=none; rua=mailto:postmaster@yourdomain.com"
```

**DKIM Record (after installation):**
```bash
# Generate DKIM keys
docker exec mailserver setup config dkim

# Display public key for DNS
docker exec mailserver cat /tmp/docker-mailserver/opendkim/keys/yourdomain.com/mail.txt

# Add as TXT record:
# Name: mail._domainkey
# Value: (the displayed key)
```

#### 2. Create Email Accounts

```bash
# Create first account
docker exec -it mailserver setup email add admin@yourdomain.com

# Add more accounts
docker exec mailserver setup email add user@yourdomain.com
docker exec mailserver setup email add support@yourdomain.com

# List all accounts
docker exec mailserver setup email list
```

#### 3. Automatic Configuration

**All services automatically use Docker-Mailserver:**
- SMTP Host: `mailserver`
- SMTP Port: `587`
- Security: STARTTLS
- Authentication: noreply@yourdomain.com
- Password: auto-generated (see `.env`)

### n8n Integration Setup

**Create SMTP Credentials in n8n:**

1. Open n8n: `https://n8n.yourdomain.com`
2. Settings → Credentials → Add New
3. Credential Type: SMTP
4. Configuration:

```
Host: mailserver
Port: 587
User: noreply@yourdomain.com
Password: [see .env file - MAIL_NOREPLY_PASSWORD]
SSL/TLS: Enable STARTTLS
Sender Email: noreply@yourdomain.com
```

**Internal URL for HTTP Requests:** `http://mailserver:587`

### Example Workflows

#### Example 1: Send Production Email

```javascript
// 1. Manual Trigger Node

// 2. Send Email Node
// → Select SMTP credential (see setup above)
{
  "to": "customer@example.com",
  "subject": "Order Confirmation #12345",
  "html": `
    <h1>Thank you for your order!</h1>
    <p>Your order has been successfully processed.</p>
    <p>Order Number: #12345</p>
  `
}

// Email sent via Docker-Mailserver
// Recipient receives real email
```

#### Example 2: Cal.com Booking Notifications

```javascript
// Cal.com automatically sends emails via Docker-Mailserver:
// - Booking confirmations
// - Calendar invitations (.ics)
// - Reminders
// - Cancellations/rescheduling

// No configuration needed - automatic!
// All Cal.com emails → Docker-Mailserver → Recipients
```

#### Example 3: Invoice Ninja Integration

```javascript
// Configure SMTP in Invoice Ninja:
// Settings → Email Settings → SMTP Configuration
// Host: mailserver
// Port: 587
// Encryption: TLS
// Username: noreply@yourdomain.com
// Password: [from .env]

// Workflow example:
// 1. Invoice Ninja creates invoice
// 2. Invoice Ninja sends email via Docker-Mailserver
// 3. Customer receives professional invoice via email
```

### Troubleshooting

**Emails not being delivered:**

```bash
# 1. Check DNS records
nslookup -type=MX yourdomain.com
nslookup -type=TXT yourdomain.com

# 2. Check Docker-Mailserver logs
docker logs mailserver --tail 100

# 3. Check mail queue
docker exec mailserver postqueue -p

# 4. Check DKIM status
docker exec mailserver setup config dkim status

# 5. Send test email
docker exec mailserver setup email add test@yourdomain.com
# Then send from external to test@yourdomain.com
```

**SMTP authentication fails:**

```bash
# 1. Check account exists
docker exec mailserver setup email list

# 2. Test authentication
docker exec mailserver doveadm auth test noreply@yourdomain.com [password]

# 3. Verify password in .env
grep MAIL_NOREPLY_PASSWORD .env

# 4. Restart service
docker compose restart mailserver
```

**Spam issues (emails landing in spam):**

```bash
# 1. Check DKIM, SPF, DMARC
# Use online tools: https://mxtoolbox.com/

# 2. Check IP reputation
# https://multirbl.valli.org/

# 3. Check Rspamd logs
docker exec mailserver cat /var/log/rspamd/rspamd.log

# 4. Test outgoing port 25
telnet smtp.gmail.com 25
```

**Docker-Mailserver won't start:**

```bash
# 1. Check logs
docker logs mailserver --tail 100

# 2. Check volumes
docker volume ls | grep mailserver

# 3. Check ports (25, 465, 587, 993)
sudo netstat -tulpn | grep -E "25|465|587|993"

# 4. Recreate container
docker compose up -d --force-recreate mailserver
```

### Resources

- **GitHub:** https://github.com/docker-mailserver/docker-mailserver
- **Documentation:** https://docker-mailserver.github.io/docker-mailserver/latest/
- **Setup Guide:** https://docker-mailserver.github.io/docker-mailserver/latest/usage/
- **Best Practices:** https://docker-mailserver.github.io/docker-mailserver/latest/faq/

</details>

<details>
<summary><b>✉️ SnappyMail - Webmail Client</b></summary>

### What is SnappyMail?

SnappyMail is a modern, ultra-fast webmail client with only 138KB load time. It provides a complete email interface for Docker-Mailserver with professional features like PGP encryption and multi-account support.

### Features

- **Ultra-fast Performance:** 138KB initial load, 99% Lighthouse score
- **Multiple Accounts:** Manage multiple email accounts in one interface
- **Mobile Responsive:** Works perfectly on all devices
- **PGP Encryption:** Built-in support for encrypted emails
- **2-Factor Authentication:** Enhanced security for webmail access
- **No Database Required:** Simple file-based configuration
- **Dark Mode:** Built-in theme support

### Initial Setup

**Prerequisite:** Docker-Mailserver must be installed (SnappyMail requires IMAP/SMTP).

#### 1. Get Admin Password

```bash
# Display admin password
docker exec snappymail cat /var/lib/snappymail/_data_/_default_/admin_password.txt
```

#### 2. Configure Admin Panel

1. Open admin panel: `https://webmail.yourdomain.com/?admin`
2. Username: `admin`
3. Password: (from step 1)

#### 3. Add Domain

In the admin panel:

**Domains → Add Domain:**
```
Domain: yourdomain.com
IMAP Server: mailserver
IMAP Port: 143
IMAP Security: STARTTLS
SMTP Server: mailserver
SMTP Port: 587
SMTP Security: STARTTLS
```

#### 4. User Login

After domain configuration, users can log in:

1. URL: `https://webmail.yourdomain.com`
2. Email: `user@yourdomain.com`
3. Password: (User's Docker-Mailserver password)

### n8n Integration Setup

**SnappyMail is a webmail client without a direct API.** Integration happens via Docker-Mailserver:

**Email Workflow Architecture:**
```
n8n Send Email Node → Docker-Mailserver → SnappyMail (read emails)
```

**IMAP Integration in n8n (retrieve emails):**

1. Email (IMAP) Trigger Node in n8n
2. Configuration:

```
Host: mailserver
Port: 993
User: user@yourdomain.com
Password: [Docker-Mailserver Password]
TLS: Enabled
```

**Internal URLs:**
- IMAP: `mailserver:993` (with TLS) or `mailserver:143` (STARTTLS)
- SMTP: `mailserver:587` (STARTTLS)

### Example Workflows

#### Example 1: Email Management Workflow

```javascript
// SnappyMail Use Case: Manage emails via web UI

// Workflow Architecture:
// 1. Service sends email → Docker-Mailserver
// 2. User opens SnappyMail → Reads email
// 3. User replies → Sent via Docker-Mailserver

// n8n Parallel Workflow:
// 1. IMAP Trigger Node (mailserver:993)
//    → Automatically process new emails
// 2. Code Node - Analyze email
// 3. Conditional Node - Filter by criteria
// 4. Action Nodes - Automated actions
```

#### Example 2: Multi-Account Management

```javascript
// SnappyMail Feature: Manage multiple accounts

// Setup in SnappyMail:
// 1. User Login: user@yourdomain.com
// 2. Settings → Accounts → Add Account
// 3. Add more accounts (support@, sales@, etc.)
// 4. Switch between accounts with one click

// Manage all emails centrally!
```

#### Example 3: Ticket System Integration

```javascript
// 1. IMAP Trigger Node (mailserver:993)
//    Mailbox: support@yourdomain.com
//    → Waits for new support emails

// 2. Code Node - Extract ticket data
const ticketData = {
  from: $json.from.value[0].address,
  subject: $json.subject,
  body: $json.textPlain || $json.textHtml,
  date: $json.date,
  priority: $json.subject.includes('URGENT') ? 'high' : 'normal'
};
return ticketData;

// 3. HTTP Request Node - Create ticket
// POST to ticketing system API
{
  "title": ticketData.subject,
  "description": ticketData.body,
  "customer_email": ticketData.from,
  "priority": ticketData.priority
}

// 4. Send Email Node - Send confirmation
// → Customer receives ticket number
// → Email visible in SnappyMail

// Support team can reply in SnappyMail!
```

### Troubleshooting

**SnappyMail Web UI not accessible:**

```bash
# 1. Check container status
docker ps | grep snappymail
# Should show: STATUS = Up

# 2. Check logs
docker logs snappymail --tail 50

# 3. Get admin password again
docker exec snappymail cat /var/lib/snappymail/_data_/_default_/admin_password.txt

# 4. Check Caddy logs
docker logs caddy | grep snappymail

# 5. Restart container
docker compose restart snappymail
```

**Users cannot log in:**

```bash
# 1. Check domain configuration
# → Open admin panel: https://webmail.yourdomain.com/?admin
# → Domains → Check domain
# → Verify IMAP/SMTP settings

# 2. Check user account in Docker-Mailserver
docker exec mailserver setup email list

# 3. Test IMAP/SMTP connection
docker exec snappymail nc -zv mailserver 143
docker exec snappymail nc -zv mailserver 587

# 4. Test authentication
docker exec mailserver doveadm auth test user@yourdomain.com [password]

# 5. Check user-specific logs
docker logs snappymail | grep -i "login\|auth\|imap"
```

**Emails not showing:**

```bash
# 1. Check IMAP connection
docker exec snappymail nc -zv mailserver 143

# 2. Check mailbox in Docker-Mailserver
docker exec mailserver doveadm mailbox list -u user@yourdomain.com

# 3. Test email delivery
# Send test email to user@yourdomain.com

# 4. Check Docker-Mailserver logs
docker logs mailserver | grep user@yourdomain.com

# 5. Clear SnappyMail cache
docker exec snappymail rm -rf /var/lib/snappymail/_data_/_default_/cache/*
docker compose restart snappymail
```

**Performance issues:**

```bash
# 1. Check cache size
docker exec snappymail du -sh /var/lib/snappymail/_data_/_default_/cache/

# 2. Clear cache (if too large)
docker exec snappymail rm -rf /var/lib/snappymail/_data_/_default_/cache/*

# 3. Check container resources
docker stats snappymail --no-stream

# 4. Check logs for errors
docker logs snappymail | grep -i "error\|warning"

# 5. Restart container
docker compose restart snappymail
```

### Resources

- **GitHub:** https://github.com/the-djmaze/snappymail
- **Documentation:** https://snappymail.eu/docs/
- **Demo:** https://snappymail.eu/demo/
- **Admin Guide:** https://snappymail.eu/docs/admin/
- **Web-UI:** `https://webmail.yourdomain.com`
- **Admin Panel:** `https://webmail.yourdomain.com/?admin`

</details>

### Workflow Automation

<details>
<summary><b>🔧 n8n - Workflow Automation Platform</b></summary>

### What is n8n?

n8n is a powerful, extendable workflow automation platform that lets you connect anything to everything via its open, fair-code model. It's the heart of AI LaunchKit, orchestrating all integrations between the 50+ services.

### Features

- **400+ Integrations:** Pre-built nodes for popular services
- **Visual Workflow Editor:** Drag-and-drop interface for building automations
- **Custom Code Execution:** JavaScript/Python nodes for complex logic
- **Self-Hosted:** Full data control, no external dependencies
- **Active Community:** 300+ pre-built workflow templates included
- **Advanced Scheduling:** Cron expressions, intervals, webhook triggers
- **Error Handling:** Built-in retry logic, error workflows, monitoring

### Initial Setup

**First Login to n8n:**

1. Navigate to `https://n8n.yourdomain.com`
2. **First visitor becomes owner** - Create your admin account
3. Set strong password (minimum 8 characters)
4. Setup complete!

**Generate API Key (for external integrations):**

1. Click your profile (bottom left)
2. Settings → API
3. Create new API Key
4. Save securely - used for n8n-MCP and external automations

### n8n Integration Setup

n8n integrates with itself and other AI LaunchKit services:

#### Connect to Internal Services

**All services are pre-configured with internal URLs:**

```javascript
// PostgreSQL (internal database)
Host: postgres
Port: 5432
Database: n8n
User: n8n
Password: [from .env file]

// Redis (queue management)
Host: redis
Port: 6379

// Ollama (local LLMs)
Base URL: http://ollama:11434

// Mailpit (email testing)
SMTP Host: mailpit
SMTP Port: 1025
```

#### API Access from External Tools

```bash
# n8n API endpoint (external)
https://n8n.yourdomain.com/api/v1

# Authentication header
Authorization: Bearer YOUR_API_KEY

# Example: List all workflows
curl -X GET https://n8n.yourdomain.com/api/v1/workflows \
  -H "Authorization: Bearer YOUR_API_KEY"
```

### Example Workflows

#### Example 1: AI Email Processing Pipeline

Complete workflow for intelligent email handling:

```javascript
// 1. Email (IMAP) Trigger Node
Host: mailserver (or mailpit for testing)
Port: 993
TLS: Enabled
Check for new emails every: 1 minute

// 2. Code Node - Extract Email Data
const email = {
  from: $json.from.value[0].address,
  subject: $json.subject,
  body: $json.textPlain || $json.html,
  date: $json.date,
  attachments: $json.attachments ? $json.attachments.length : 0
};

// Classify email priority
const urgent = /urgent|asap|important/i.test(email.subject);
email.priority = urgent ? 'high' : 'normal';

return { json: email };

// 3. OpenAI Node - Analyze Email Content
Operation: Message a Model
Model: gpt-4o-mini
Messages:
  System: "You are an email classification assistant. Categorize emails into: Support, Sales, General, Spam"
  User: "Subject: {{$json.subject}}\n\nBody: {{$json.body}}"

// 4. Switch Node - Route by Category
Mode: Rules
Rules:
  - category equals "Support" → Route to support workflow
  - category equals "Sales" → Route to CRM
  - category equals "Spam" → Delete
  - default → Archive

// 5a. Support Route: Create Ticket
// HTTP Request to ticketing system
Method: POST
URL: http://baserow:8000/api/database/rows/table/tickets/
Body: {
  "title": "{{$('Extract Email').json.subject}}",
  "description": "{{$('Extract Email').json.body}}",
  "customer_email": "{{$('Extract Email').json.from}}",
  "priority": "{{$('Extract Email').json.priority}}",
  "status": "New"
}

// 6. Send Email Node - Auto-Reply
To: {{$('Extract Email').json.from}}
Subject: Re: {{$('Extract Email').json.subject}}
Message: |
  Thank you for contacting us!
  
  Your ticket #{{$json.id}} has been created.
  Our team will respond within 24 hours.
  
  Best regards,
  Support Team
```

#### Example 2: Multi-Service Data Sync

Sync data across multiple services automatically:

```javascript
// 1. Schedule Trigger Node
Trigger Interval: Every 15 minutes
Cron Expression: */15 * * * *

// 2. HTTP Request - Get New Customers from Supabase
Method: GET
URL: http://supabase-kong:8000/rest/v1/customers
Headers:
  apikey: {{$env.SUPABASE_ANON_KEY}}
  Authorization: Bearer {{$env.SUPABASE_ANON_KEY}}
Query Parameters:
  select: *
  created_at: gte.{{$now.minus(15, 'minutes').toISO()}}

// 3. Loop Over Items Node
// Process each new customer

// 4. Branch 1: Create in CRM (Twenty)
HTTP Request Node
Method: POST
URL: http://twenty:3000/graphql
Body (GraphQL):
mutation {
  createPerson(data: {
    firstName: "{{$json.first_name}}"
    lastName: "{{$json.last_name}}"
    email: "{{$json.email}}"
    phone: "{{$json.phone}}"
    companyId: "{{$json.company_id}}"
  }) {
    id
  }
}

// 5. Branch 2: Add to Mailing List (Mautic)
HTTP Request Node  
Method: POST
URL: http://mautic_web/api/contacts/new
Body: {
  "email": "{{$json.email}}",
  "firstname": "{{$json.first_name}}",
  "lastname": "{{$json.last_name}}",
  "tags": ["new-customer", "supabase-sync"]
}

// 6. Branch 3: Create Project (Leantime)
HTTP Request Node
Method: POST
URL: http://leantime:8080/api/jsonrpc
Body: {
  "jsonrpc": "2.0",
  "method": "leantime.rpc.projects.addProject",
  "params": {
    "values": {
      "name": "Onboarding - {{$json.company_name}}",
      "clientId": 1,
      "state": 0
    }
  },
  "id": 1
}

// 7. Slack Notification
Channel: #new-customers
Message: |
  🎉 New Customer Added!
  
  Name: {{$json.first_name}} {{$json.last_name}}
  Email: {{$json.email}}
  Company: {{$json.company_name}}
  
  Actions completed:
  ✅ Added to CRM
  ✅ Added to mailing list
  ✅ Onboarding project created
```

#### Example 3: AI Content Generation Pipeline

Generate and publish content automatically:

```javascript
// 1. Schedule Trigger
Trigger: Weekly on Monday at 10 AM

// 2. Code Node - Define Content Topics
const topics = [
  "AI automation trends",
  "Self-hosted tools benefits",
  "Workflow optimization tips",
  "Data privacy best practices"
];

// Random topic selection
const randomTopic = topics[Math.floor(Math.random() * topics.length)];

return {
  json: {
    topic: randomTopic,
    date: new Date().toISOString()
  }
};

// 3. OpenAI Node - Generate Blog Post
Operation: Message a Model
Model: gpt-4o
Messages:
  System: "You are a technical content writer specializing in AI and automation."
  User: |
    Write a comprehensive blog post about: {{$json.topic}}
    
    Requirements:
    - 800-1000 words
    - Include practical examples
    - SEO-optimized with relevant keywords
    - Engaging tone for technical audience
    - Include 3-5 actionable takeaways

// 4. OpenAI Node - Generate Social Media Posts
Operation: Message a Model
Model: gpt-4o-mini
Messages:
  User: |
    Create social media posts for this blog:
    {{$('Generate Blog Post').json.choices[0].message.content}}
    
    Create:
    1. LinkedIn post (max 1300 characters)
    2. Twitter thread (3-5 tweets)
    3. Instagram caption (max 2200 characters)

// 5. HTTP Request - Publish to WordPress/Ghost
Method: POST
URL: http://wordpress:80/wp-json/wp/v2/posts
Headers:
  Authorization: Basic {{$env.WORDPRESS_AUTH}}
Body: {
  "title": "{{$json.topic}}",
  "content": "{{$('Generate Blog Post').json.content}}",
  "status": "draft",
  "categories": [1]
}

// 6. Postiz Node - Schedule Social Posts
// Use native Postiz node or HTTP requests
// Schedule LinkedIn, Twitter, Instagram posts

// 7. Slack Notification
Channel: #content-team
Message: |
  📝 New Blog Post Generated!
  
  Topic: {{$('Define Topics').json.topic}}
  Status: Draft (ready for review)
  WordPress: {{$('Publish').json.link}}
  
  Social posts scheduled ✅
```

### Troubleshooting

**Workflows not executing:**

```bash
# 1. Check n8n container status
docker ps | grep n8n

# 2. Check n8n logs
docker logs n8n --tail 100

# 3. Check worker processes
docker logs n8n-worker --tail 100

# 4. Verify Redis connection
docker exec n8n nc -zv redis 6379

# 5. Check PostgreSQL connection
docker exec n8n nc -zv postgres 5432
```

**"Service not reachable" errors:**

```bash
# 1. Verify internal service is running
docker ps | grep [service-name]

# 2. Test internal DNS resolution
docker exec n8n ping [service-name]

# 3. Check Docker network
docker network inspect ai-launchkit_default

# 4. Verify port is correct
docker port [service-name]

# 5. Check service logs
docker logs [service-name] --tail 50
```

**Memory/Performance issues:**

```bash
# 1. Check resource usage
docker stats n8n --no-stream

# 2. Check worker count
grep N8N_WORKER_COUNT .env

# 3. Increase memory limit (if needed)
# Edit docker-compose.yml:
# mem_limit: 2g

# 4. Optimize workflows
# - Use pagination for large datasets
# - Add Wait nodes between bulk operations
# - Split complex workflows into smaller ones

# 5. Clear execution data
docker exec n8n n8n clear:executions --all
```

**Credential authentication failures:**

```bash
# 1. Check credential configuration
# In n8n: Credentials → Test Connection

# 2. Verify environment variables
docker exec n8n printenv | grep [SERVICE]

# 3. Check internal URLs
# Use service name, not localhost
# ✅ http://mailserver:587
# ❌ http://localhost:587

# 4. Recreate credential
# Delete and recreate in n8n UI

# 5. Restart n8n
docker compose restart n8n
```

**Webhook not receiving data:**

```bash
# 1. Test webhook URL
curl -X POST https://n8n.yourdomain.com/webhook-test/your-webhook \
  -H "Content-Type: application/json" \
  -d '{"test": "data"}'

# 2. Check Caddy logs
docker logs caddy | grep webhook

# 3. Verify webhook is active
# n8n → Workflow → Webhook node → Check "Listening"

# 4. Check firewall
sudo ufw status | grep 443

# 5. Test from external service
# Verify webhook URL is accessible from internet
```

### Resources

- **Official Documentation:** https://docs.n8n.io/
- **Community Forum:** https://community.n8n.io/
- **Workflow Templates:** https://n8n.io/workflows
- **API Documentation:** https://docs.n8n.io/api/
- **YouTube Tutorials:** https://www.youtube.com/@n8n-io
- **GitHub:** https://github.com/n8n-io/n8n

### Best Practices

**Workflow Organization:**
- Use descriptive workflow names
- Add notes to complex nodes
- Group related nodes with sticky notes
- Use consistent naming for credentials
- Version control: Export workflows as JSON

**Performance Optimization:**
- Use batch processing for large datasets
- Add Wait nodes between API calls
- Implement error handling with Try/Catch nodes
- Use pagination for API requests
- Monitor execution times

**Security:**
- Never hardcode credentials in workflows
- Use environment variables for sensitive data
- Implement webhook authentication
- Regularly rotate API keys
- Review workflow permissions

**Maintenance:**
- Regularly check error executions
- Monitor workflow execution times
- Update community nodes
- Backup workflows weekly
- Document complex logic in notes

</details>

<details>
<summary><b>🤖 n8n-MCP - AI Workflow Generator</b></summary>

### What is n8n-MCP?

n8n-MCP enables AI assistants like Claude Desktop and Cursor to generate complete n8n workflows through natural language. It provides access to documentation for 525+ n8n nodes, allowing AI tools to understand node properties, authentication requirements, and configuration options.

n8n-MCP implements the Model Context Protocol (MCP) standard, making it compatible with any MCP-enabled AI tool.

### Features

- **Complete node documentation** - Properties, authentication, and examples for 525+ nodes
- **Workflow generation** - Create complex automations from natural language prompts
- **Validation** - Ensures correct node configuration before deployment
- **99% coverage** - Supports nearly all n8n node properties and settings
- **MCP standard** - Works with any MCP-compatible AI tool (Claude, Cursor, etc.)

### Initial Setup

**Access n8n-MCP:**
- **External URL:** `https://n8nmcp.yourdomain.com`
- **Internal URL:** `http://n8nmcp:3000`
- **Token:** Found in `.env` file as `N8N_MCP_TOKEN`

**No web interface** - n8n-MCP is a backend service accessed through AI tools.

### Setup with Claude Desktop

**1. Locate Claude Desktop Config File:**

**macOS/Linux:**
```bash
~/.config/claude/claude_desktop_config.json
```

**Windows:**
```
%APPDATA%\Claude\claude_desktop_config.json
```

**2. Configure Claude Desktop:**

```json
{
  "mcpServers": {
    "n8n-mcp": {
      "command": "npx",
      "args": ["@czlonkowski/n8n-mcp-client"],
      "env": {
        "N8N_MCP_URL": "https://n8nmcp.yourdomain.com",
        "N8N_MCP_TOKEN": "your-token-from-env-file",
        "N8N_API_URL": "https://n8n.yourdomain.com",
        "N8N_API_KEY": "your-n8n-api-key"
      }
    }
  }
}
```

**3. Restart Claude Desktop**

### Setup with Cursor IDE

**Create `.cursor/mcp_config.json` in your project:**

```json
{
  "servers": {
    "n8n-mcp": {
      "url": "https://n8nmcp.yourdomain.com",
      "token": "your-token-from-env-file"
    }
  }
}
```

### Example Prompts for Claude/Cursor

#### Basic Automation

```
"Create an n8n workflow that monitors a Gmail inbox for invoices, 
extracts data using AI, and saves to Google Sheets"
```

**Claude will:**
1. Use n8n-MCP to look up node documentation
2. Generate complete workflow JSON
3. Configure all node properties correctly
4. Include authentication requirements
5. Provide deployment instructions

#### Complex Integration

```
"Build a workflow that:
1. Triggers on new Stripe payment
2. Creates invoice in QuickBooks
3. Sends receipt via SendGrid
4. Updates customer in Airtable
5. Posts to Slack channel"
```

**Result:** Complete workflow with all nodes configured, including:
- Webhook trigger
- API credentials
- Data transformations
- Error handling
- Notification logic

#### AI Pipeline

```
"Design a content pipeline that takes YouTube videos, 
transcribes with Whisper, summarizes with GPT-4, 
and posts to WordPress with SEO optimization"
```

**Claude generates:**
- YouTube data extraction
- Whisper transcription node
- OpenAI summarization
- WordPress API integration
- SEO metadata generation

### Available MCP Commands

n8n-MCP provides these commands to AI assistants:

**`list_nodes`** - Get all available n8n nodes
```json
Response: {
  "nodes": ["HTTP Request", "Code", "IF", "Gmail", "Slack", ...]
}
```

**`get_node_docs`** - Full documentation for specific node
```json
Request: { "node": "HTTP Request" }
Response: {
  "properties": [...],
  "authentication": [...],
  "examples": [...]
}
```

**`validate_workflow`** - Check workflow configuration
```json
Request: { "workflow": {...} }
Response: {
  "valid": true,
  "errors": []
}
```

**`suggest_nodes`** - Get node recommendations for task
```json
Request: { "task": "send email with attachment" }
Response: {
  "nodes": ["Gmail", "Send Email", "IMAP"],
  "reasoning": "..."
}
```

### n8n Integration

**HTTP Request to n8n-MCP from n8n workflow:**

```javascript
// HTTP Request Node Configuration
Method: POST
URL: https://n8nmcp.yourdomain.com/generate
Authentication: Header Auth
  Header: Authorization
  Value: Bearer {{$env.N8N_MCP_TOKEN}}
  
Body (JSON):
{
  "prompt": "Create workflow to sync Notion database with Google Calendar",
  "target_n8n": "https://n8n.yourdomain.com",
  "auto_import": true
}

// Response:
{
  "workflow": {...},
  "import_url": "https://n8n.yourdomain.com/workflows/import",
  "validation": { "valid": true }
}
```

### Example: AI-Generated Workflow

**Prompt to Claude:**
```
"Create an n8n workflow that:
1. Watches a folder in Google Drive
2. When a new PDF is added, extract text with OCR
3. Summarize the content with OpenAI
4. Create a task in Vikunja with the summary
5. Send notification to Slack"
```

**Claude with n8n-MCP generates:**

```javascript
// 1. Google Drive Trigger Node
Trigger: On File Created
Folder: "/Invoices"
File Type: PDF

// 2. HTTP Request Node - OCR Service
Method: POST
URL: http://tesseract:8000/ocr
Body: 
  file: {{$binary.data}}
  language: eng

// 3. OpenAI Node - Summarization
Operation: Message a Model
Model: gpt-4o-mini
System Message: "Summarize this invoice in 2-3 sentences"
User Message: {{$json.text}}

// 4. HTTP Request Node - Vikunja API
Method: POST
URL: http://vikunja:3456/api/v1/tasks
Headers:
  Authorization: Bearer {{$credentials.vikunjaToken}}
Body:
{
  "title": "Invoice: {{$('Google Drive').json.name}}",
  "description": "{{$json.summary}}",
  "project_id": 1
}

// 5. Slack Node
Operation: Send Message
Channel: #finance
Message: |
  New invoice processed:
  File: {{$('Google Drive').json.name}}
  Summary: {{$('OpenAI').json.summary}}
  Task: {{$('Vikunja').json.link}}
```

### Tips for Best Results

**Be Specific:**
```
❌ "Create a workflow to process emails"
✅ "Create a workflow that reads unread Gmail emails, 
   extracts attachments, uploads to Google Drive, 
   and marks email as read"
```

**Include Tool Names:**
```
❌ "Send data to my CRM"
✅ "Send data to Odoo CRM via HTTP Request node"
```

**Provide Sample Data:**
```
"Process customer data like:
{
  'name': 'John Doe',
  'email': 'john@example.com',
  'company': 'Acme Corp'
}"
```

**Iterate Through Conversation:**
```
1. "Create workflow to process invoices"
2. [Claude generates initial workflow]
3. "Add error handling and retry logic"
4. [Claude enhances workflow]
5. "Add notification to Microsoft Teams instead of Slack"
6. [Claude updates notification node]
```

### Workflow Version Control

**Export Workflows as JSON:**

```bash
# After AI generates workflow, export it
curl -X GET https://n8n.yourdomain.com/api/v1/workflows/123 \
  -H "Authorization: Bearer YOUR_API_KEY" \
  > workflow-v1.json

# Commit to Git
git add workflow-v1.json
git commit -m "Add AI-generated invoice processing workflow"
```

### Troubleshooting

**Connection refused:**
```bash
# Check n8n-MCP is running
docker ps | grep n8nmcp

# Check token in .env
grep N8N_MCP_TOKEN .env

# Test connection
curl -H "Authorization: Bearer YOUR_TOKEN" \
  https://n8nmcp.yourdomain.com/health
```

**Invalid workflow generated:**
```bash
# Use validation endpoint
curl -X POST https://n8nmcp.yourdomain.com/validate \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -d '{"workflow": {...}}'

# Check n8n-MCP logs
docker logs n8nmcp --tail 100
```

**Missing node documentation:**
```bash
# Update n8n-MCP to latest version
docker compose pull n8nmcp
docker compose up -d n8nmcp

# Rebuild node cache
docker exec n8nmcp npm run rebuild-cache
```

**Timeout errors:**
```bash
# Increase timeout in MCP client config
{
  "mcpServers": {
    "n8n-mcp": {
      ...
      "timeout": 60000
    }
  }
}
```

### Resources

- **Documentation:** https://github.com/czlonkowski/n8n-mcp
- **MCP Protocol:** https://modelcontextprotocol.io
- **n8n API Reference:** https://docs.n8n.io/api/
- **Community Examples:** https://n8n.io/workflows (filter by "AI-generated")

### Best Practices

**Prompt Engineering:**
- Start with high-level description
- Add details incrementally
- Test each addition
- Use real data examples
- Specify error handling requirements

**Security:**
- Never include credentials in prompts
- Use n8n credential system
- Validate AI-generated workflows before production
- Review generated code for security issues

**Maintenance:**
- Export workflows to Git after generation
- Document prompt used to generate workflow
- Test generated workflows thoroughly
- Keep n8n-MCP updated for latest node support

**Performance:**
- Break complex workflows into smaller ones
- Use webhook triggers instead of polling where possible
- Implement rate limiting for external APIs
- Monitor workflow execution times

</details>

### User Interfaces

<details>
<summary><b>💬 Open WebUI - ChatGPT Interface</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📱 Postiz - Social Media Management</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### Video Conferencing

<details>
<summary><b>📹 Jitsi Meet - Video Conferencing</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### Business & Productivity

<details>
<summary><b>📅 Cal.com - Scheduling Platform</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>✅ Vikunja - Task Management</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🎯 Leantime - Project Management</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>⏱️ Kimai - Time Tracking</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>💰 Invoice Ninja - Invoicing Platform</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📊 Baserow - Airtable Alternative</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📋 NocoDB - Airtable Alternative</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📝 Formbricks - Survey Platform</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📈 Metabase - Business Intelligence</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🏢 Odoo 18 - ERP/CRM</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>💼 Twenty CRM - Modern CRM</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📞 EspoCRM - CRM Platform</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📧 Mautic - Marketing Automation</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### AI Content Generation

<details>
<summary><b>🎨 ComfyUI - Image Generation</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### AI-Powered Development

<details>
<summary><b>⚡ bolt.diy - AI App Builder</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🎨 OpenUI - UI Component Generator</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### AI Agents

<details>
<summary><b>🤖 Flowise - Visual AI Builder</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🎙️ LiveKit - Voice Agents</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🧠 Dify - LLMOps Platform</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>💾 Letta - Stateful Agents</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🌐 Browser-use - Browser Control</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>👁️ Skyvern - Vision Automation</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🖥️ Browserless - Headless Chrome</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### RAG Systems

<details>
<summary><b>📚 RAGApp - RAG Assistant Builder</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🔍 Qdrant - Vector Database</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🗄️ Weaviate - AI Vector Database</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### Speech & Language

<details>
<summary><b>🎤 Faster-Whisper - Speech-to-Text</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🔊 OpenedAI-Speech - Text-to-Speech</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🗣️ TTS Chatterbox - Advanced TTS</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🌍 LibreTranslate - Translation API</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>👁️ OCR Bundle - Text Extraction</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📝 Scriberr - Audio Transcription</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📞 Vexa - Meeting Transcription</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### Search & Web Data

<details>
<summary><b>🔍 SearXNG - Privacy Search</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🔎 Perplexica - AI Search</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🕷️ Crawl4Ai - Web Crawler</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📊 GPT Researcher - Research Agent</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🔬 Local Deep Research - Iterative Research</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### Knowledge Graphs

<details>
<summary><b>🕸️ Neo4j - Graph Database</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🔗 LightRAG - Graph-Based RAG</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### Media Processing Suite

<details>
<summary><b>🎬 Media Processing Tools</b></summary>

<!-- TODO: Content will be added in Phase 2 -->
**Tools included:**
- FFmpeg
- ImageMagick
- ExifTool
- MediaInfo
- SoX
- Ghostscript
- Python3 with libraries

</details>

### Data Infrastructure

<details>
<summary><b>🔥 Supabase - Firebase Alternative</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🐘 PostgreSQL - Relational Database</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>⚡ Redis - In-Memory Store</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### System Management

<details>
<summary><b>🔐 Vaultwarden - Password Manager</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🌐 Caddy - Web Server</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>☁️ Cloudflare Tunnel - Secure Access</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🐍 Python Runner - Script Execution</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📊 Grafana - Metrics Visualization</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📈 Prometheus - Monitoring</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🐳 Portainer - Container Management</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### AI Support Tools

<details>
<summary><b>🦙 Ollama - Local LLMs</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📄 Gotenberg - Document Converter</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>📋 Stirling-PDF - PDF Toolkit</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

### AI Security & Compliance

<details>
<summary><b>🛡️ LLM Guard - Input/Output Filtering</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🔒 Microsoft Presidio - PII Detection (English)</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

<details>
<summary><b>🇩🇪 Flair NER - PII Detection (German)</b></summary>

<!-- TODO: Content will be added in Phase 2 -->

</details>

---

## 💡 Support & FAQ

<!-- TODO: Support section will be added in Phase 2, Step N -->

### Common Issues

<details>
<summary><b>🚨 502 Bad Gateway Errors</b></summary>

<!-- TODO: Content will be added -->

</details>

<details>
<summary><b>📧 Mail System Issues</b></summary>

<!-- TODO: Content will be added -->

</details>

<details>
<summary><b>🐳 Docker & Network Issues</b></summary>

<!-- TODO: Content will be added -->

</details>

<details>
<summary><b>⚡ Performance Issues</b></summary>

<!-- TODO: Content will be added -->

</details>

<details>
<summary><b>⚠️ General Troubleshooting</b></summary>

<!-- TODO: Content will be added -->

</details>

### Getting Help

**Community Resources:**
- **Discord**: [Join our community](https://discord.gg/ai-launchkit) *(coming soon)*
- **Forum**: [oTTomator Think Tank](https://thinktank.ottomator.ai/c/local-ai/18)
- **Issues**: [GitHub Issues](https://github.com/freddy-schuetz/ai-launchkit/issues)

**Before Creating an Issue:**
1. Check existing GitHub Issues
2. Search the Community Forum
3. Provide:
   - Your server specs
   - Services selected during installation
   - Error messages from `docker logs`
   - Output of `docker ps` and `docker stats`

---

## 🏗️ Architecture

```mermaid
graph TD
    A[Caddy - Reverse Proxy] --> B[n8n - Automation]
    A --> C[bolt.diy - AI Dev]
    A --> D[ComfyUI - Image Gen]
    A --> E[Open WebUI - Chat]
    A --> F[Other Services]
    A --> MP[Mailpit - Mail UI]
    A --> CAL[Cal.com - Scheduling]
    A --> SM[SnappyMail - Webmail]
    A --> JM[Jitsi Meet - Video]
    A --> VW[Vaultwarden - Passwords]
    
    CF[Cloudflare Tunnel] -.-> A
    
    B --> G[PostgreSQL]
    B --> H[Redis Queue]
    B --> I[Shared Storage]
    B --> PR[Python Runner]
    B --> M[Whisper ASR]
    B --> N[OpenedAI TTS]
    B --> O[Qdrant/Weaviate - Vectors]
    B --> P[Neo4j - Knowledge Graph]
    B --> LR[LightRAG - Graph RAG]
    B --> SMTP[Mail System]
    B --> CAL2[Cal.com API]
    
    CAL --> G
    CAL --> H
    CAL --> SMTP
    CAL --> JM[Jitsi Integration]
    
    JM --> JP[Jitsi Prosody - XMPP]
    JM --> JF[Jitsi Jicofo - Focus]
    JM --> JV[Jitsi JVB - WebRTC]
    JV -.-> |UDP 10000| INET[Internet]
    
    SMTP --> MP2[Mailpit SMTP]
    SMTP -.-> MS[Docker-Mailserver]
    
    SM --> MS[Docker-Mailserver IMAP/SMTP]
    
    VW --> I[Shared Storage]
    VW --> SMTP[Mail System]
    
    C --> J[Ollama - Local LLMs]
    D --> J
    E --> J
    
    K[Grafana] --> L[Prometheus]
    L --> B
    L --> G
    L --> H
```

---

## 👥 Contributors

Created and maintained by [Friedemann Schuetz](https://www.linkedin.com/in/friedemann-schuetz)

**Based on:**
- [n8n-installer](https://github.com/kossakovsky/n8n-installer) by kossakovsky
- [self-hosted-ai-starter-kit](https://github.com/n8n-io/self-hosted-ai-starter-kit) by n8n team
- [local-ai-packaged](https://github.com/coleam00/local-ai-packaged) by coleam00

[View all contributors](https://github.com/freddy-schuetz/ai-launchkit/graphs/contributors)

---

## 📜 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Ready to launch your AI projects?**

[⭐ Star this repo](https://github.com/freddy-schuetz/ai-launchkit) • [🐛 Report issues](https://github.com/freddy-schuetz/ai-launchkit/issues) • [🤝 Contribute](https://github.com/freddy-schuetz/ai-launchkit/pulls)

</div>
