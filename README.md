# SCTC Sources

Public content source repository for the TSAIC website.

## Structure

- `content.json`: main data file consumed by website frontend
- `stories/*.md`: markdown story articles referenced by `content.json -> stories[].markdown_path`

## Required Fields

### Member

- `image_link` (required)
- `name` (required)
- `intro` (required)
- optional: `ig`, `yt`, `linkedin`, `threads`, `personal_website`

### Event

- `event_name`
- `event_date`
- `event_time`
- `location_name`
- optional: `location_link`
- optional: `register_link`
- `schedule` (array of strings)
- optional: `notice`

### Social

All optional:

- `ig`
- `threads`
- `discord`
- `email_link`

### Vision

- `why_exist` (array of paragraphs)
- `what_doing` (array of points)

### Story

- `publish_date`
- `publisher`
- `image_link`
- `title`
- `sub_title`
- `markdown_path` (path to markdown file inside this repository)

### Community

- `community.abbreviation`: short brand text for navbar
- `community.full_name`: full brand text for hero/footer

## Editing Notes

- Dates should use ISO format `YYYY-MM-DD`.
- Keep markdown readable with headings and short sections.
- Use absolute URLs for external links and images.
