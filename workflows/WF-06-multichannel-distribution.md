## WF-06 — Multi-Channel Content Distribution
### Phase: EXECUTE
### Version: 1.0
#
### TRIGGER: Every time a new long-form piece is published
### OUTPUT:  5 channel-specific content pieces ready to schedule
### TIME:    30 min per article
##### ──────────────────────────────────────────────────────────────

## Step 1 — Human: Confirm Publish + Share URL
Confirm the article is live and indexed. Share the URL with the ops team.

## Step 2 — Claude: Generate Distribution Pack
**Prompt to use:** `prompts/execute/11-multichannel-distribution.md`
**Input:** Published article URL or full text

**Outputs produced:**
1. LinkedIn post (150–250 words)
2. X/Twitter thread (3–5 tweets)
3. Newsletter snippet (100–150 words)
4. Social card copy (headline + subheadline)
5. Internal Slack summary (3 bullets)

## Step 3 — Human: Review + Schedule
- [ ] Voice matches CLIENT_VOICE for each channel?
- [ ] LinkedIn: link in first comment (not in post body)?
- [ ] Stats or claims in social copy are accurate?
- [ ] Schedule LinkedIn and X within 24–48 hours of publish
- [ ] Newsletter snippet queued for next send
- [ ] Social card copy sent to design team with article link

---

---
