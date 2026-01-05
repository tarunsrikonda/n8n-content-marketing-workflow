# Troubleshooting

## Common Issues

| Error | Cause | Fix |
|-------|-------|-----|
| "Add your API key here" | Missing credentials | See `CREDENTIALS-SETUP.md` |
| Postiz 401 | Wrong API key | Regenerate Postiz Public API key |
| Brevo 400 | List ID=7 missing | Create list ID 7 in Brevo |
| WP 401 | App password wrong | Regenerate WP Application Password |
| Groq rate limit | Too many runs | Increase Schedule Trigger interval |

## Test Each Section
1. Execute up to "Create WP Post" → Check WP drafts
2. Execute up to "Postiz Create" → Check Postiz dashboard
3. Execute up to "Send Brevo Email" → Check inbox
