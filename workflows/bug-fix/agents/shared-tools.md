# Shared Tools: Jira & Confluence

## Jira API
Fetch issue details, search, or read comments:

```bash
# Get issue details
bash ~/scripts/jira-fetch.sh CS-6210

# Search issues by JQL
bash ~/scripts/jira-fetch.sh search "project=CS AND status='Dev in Progress'"

# Get comments
bash ~/scripts/jira-fetch.sh comments CS-6210
```

## Confluence API
Fetch page content or search:

```bash
# Get page by ID
bash ~/scripts/confluence-fetch.sh 4591157265

# Get page by URL
bash ~/scripts/confluence-fetch.sh url "https://swingvy.atlassian.net/wiki/spaces/PS/pages/4591157265/..."

# Search
bash ~/scripts/confluence-fetch.sh search "payroll v3"
```

## Confluence Images
Download image attachments from a Confluence page:

```bash
# Download all images from a page
bash ~/scripts/confluence-images.sh 4591157265

# Download to specific directory
bash ~/scripts/confluence-images.sh 4591157265 /tmp/my-images
```

Note: Diagrams rendered by macros (draw.io, Mermaid) may not be available as downloadable images.

## When to use
- **Jira**: When you need bug details, reproduction steps, comments, or related tickets
- **Confluence**: When you need architecture docs, design specs, or technical references
- Always fetch the Jira ticket if one is mentioned in the task
- Search Confluence for relevant documentation before making architectural decisions
