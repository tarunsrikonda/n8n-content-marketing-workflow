# Setup Guide

## Prerequisites
- [ ] n8n instance (self-hosted or cloud)
- [ ] API keys: Groq, SerpAPI, Cloudflare Workers AI, FreeImage, Postiz, Brevo
- [ ] WordPress site with Application Passwords enabled

## Steps
1. **Import Workflow**
   - n8n → "+" → "Import from File"
   - Select `workflows/smarketers-content-automation-v2.json`
   - Click "Import"

2. **Add Credentials**
   | Service | Where to Add | Node Names |
   |---------|-------------|------------|
   | Groq | Credentials → Groq API | All "Groq Chat Model" nodes |
   | SerpAPI | HTTP Header (apikey) | Get Trends, Get Keywords |
   | Postiz | HTTP Header Auth | Postiz Create |
   | Brevo | HTTP Header Auth | Get Contacts, Send Email |
   | WordPress | OAuth2 API | Create WP Post |

3. **Test Run**
   - Click "Execute Workflow" 
   - Check Slack notification for success
   - Verify: WP draft → Postiz scheduled → Brevo sent

4. **Activate**
   - Toggle "Active" ON
   - Runs every 10 minutes or set your preferred time interval (Schedule Trigger)

**First run generates 3-5 posts. Scale by adjusting Loop Over Items batch size.**
