# SCTC Sources

Public content source repository for the TSAIC website.

## Structure

- `community.json`: community brand and subtitle
- `members.json`: mentor/member profile data
- `events.json`: event list and schedules
- `social.json`: social/contact links
- `vision.json`: mission and direction content
- `stories.json`: story metadata
- `stories/*.md`: markdown story articles referenced by `stories.json -> stories[].markdown_path`

## Bilingual Content (English + Traditional Chinese)

Most content fields support either:

- single-language string/array, or
- localized object with `en` and `zh-TW` keys.

Example:

```json
{
  "title": {
    "en": "Story Title",
    "zh-TW": "故事標題"
  }
}
```

## Required Fields

### Member

- `image_link` (required)
- `name` (required, localized supported)
- `intro` (required, localized supported)
- optional: `ig`, `yt`, `linkedin`, `threads`, `personal_website`

### Event

- `event_name` (localized supported)
- `event_date`
- `event_time` (localized supported)
- `location_name` (localized supported)
- optional: `location_link`
- optional: `register_link`
- `schedule` (array or localized arrays)
- optional: `notice` (localized supported)

### Social

All optional:

- `ig`
- `threads`
- `discord`
- `email_link`

### Vision

- `why_exist` (array or localized arrays)
- `what_doing` (array or localized arrays)

### Story

- `publish_date`
- `publisher` (localized supported)
- `image_link`
- `title` (localized supported)
- `sub_title` (localized supported)
- `markdown_path` (string or localized object)

Recommended `markdown_path` format:

- English: `stories/<slug>.en.md`
- Chinese: `stories/<slug>.zh-TW.md`

### Community

- `community.abbreviation`: short brand text for navbar (localized supported)
- `community.full_name`: full brand text for hero/footer (localized supported)

## Module Notes

- Frontend fetches each module file independently and composes one in-memory content object.
- Legacy `content.json` can remain as backup, but source-of-truth should be the modular files above.

## Editing Notes

- Dates should use ISO format `YYYY-MM-DD`.
- Keep markdown readable with clear headings and short sections.
- Use absolute URLs for external links and images.
