# CLIENT_CONTEXT — Fill this per client before any GrowthX task
### Version: 1.0
#
### HOW TO USE:
####   1. Duplicate this file and rename it: CLIENT_CONTEXT_[clientname].md
####   2. Fill in every field below
####   3. Paste the filled block at the top of your first Claude message
####      in any session. This is the only thing that changes between clients.
##### ─────────────────────────────────────────────────────────────────────

CLIENT_CONTEXT:
  client_name:         ""        # e.g. "Abnormal AI"
  website_url:         ""        # e.g. "https://abnormalsecurity.com"
  product_category:    ""        # e.g. "AI email security platform"
  icp_role:            ""        # e.g. "CISOs and IT Security Managers at mid-market companies"
  icp_pain:            ""        # e.g. "legacy email filters miss AI-generated phishing attacks"
  primary_competitors: []        # e.g. ["Proofpoint", "Mimecast", "Abnormal"]
  current_da:          ""        # Domain Authority (0–100). Check ahrefs or Moz.
  monthly_sessions:    ""        # Current organic sessions baseline (from GA4 or GSC)
  conversion_goal:     ""        # e.g. "book a demo", "start free trial", "contact sales"
  content_team_size:   ""        # e.g. "1 in-house editor + GrowthX team"
  phase:               ""        # Strategy / Build / Execute / Compound
  current_top_pages:   []        # URLs of 3–5 top-performing organic pages (optional)
  target_verticals:    []        # e.g. ["financial services", "healthcare", "enterprise SaaS"]

CLIENT_VOICE:
  tone:           ""             # e.g. "confident but approachable", "technical and precise"
  pov:            ""             # e.g. "operator", "researcher", "challenger brand"
  avoid:          []             # Words/phrases this client never uses
  prefer:         []             # Words/phrases this client uses consistently
  sentence_len:   ""             # short / medium / long / varied
  cta_style:      ""             # e.g. "soft ask", "direct CTA", "community invite"
  sample_urls:    []             # 2–3 URLs of existing content that exemplifies their voice

##### ─────────────────────────────────────────────────────────────────────
### EXAMPLE (filled in for a fictional client — delete before use)
##### ─────────────────────────────────────────────────────────────────────
#
#### CLIENT_CONTEXT:
####   client_name:         "Discern"
####   website_url:         "https://discernhealth.com"
####   product_category:    "Healthcare revenue cycle analytics"
####   icp_role:            "VP of Revenue Cycle at health systems with 200+ beds"
####   icp_pain:            "Can't see which claims are at risk before they deny"
####   primary_competitors: ["Waystar", "Optum360", "Availity"]
####   current_da:          "28"
####   monthly_sessions:    "4,200"
####   conversion_goal:     "book a demo"
####   content_team_size:   "0 in-house + GrowthX team"
####   phase:               "Build"
####   current_top_pages:   ["https://discernhealth.com/blog/claim-denial-rates"]
####   target_verticals:    ["health systems", "physician groups", "ASCs"]
#
#### CLIENT_VOICE:
####   tone:           "straightforward and data-driven, never condescending"
####   pov:            "operator — we've worked inside rev cycle teams"
####   avoid:          ["unlock", "game-changer", "seamless", "end-to-end solution"]
####   prefer:         ["denial rate", "clean claims", "days in AR", "first-pass yield"]
####   sentence_len:   "short"
####   cta_style:      "direct CTA"
####   sample_urls:    ["https://discernhealth.com/blog/denial-management-strategy"]
