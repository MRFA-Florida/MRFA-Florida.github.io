# MRFA Florida

Landing page for the Mayo Clinic Research Fellow’s Association (MRFA), Florida: https://mrfa-florida.github.io

## Adding a new event
1. Create the event repository from the `research-day-2026` template (green **Use this template** button), name it e.g. `research-day-2027`, edit its `data/event.json`, and turn on Pages.
2. Add an entry to `events.json` here with the date and `"url": "research-day-2027/"`.
Events move from **Upcoming** to **Past events** automatically after their date.

## Header slideshow
The campus photos rotating behind the header are listed in `index.html` (search for `Hero slideshow`). Each photo needs a full version (`name.jpg`, ~1800 px) and a phone version (`name-sm.jpg`, ~1000 px) in `assets/photos/`.

## Adding photos (gallery)
1. Upload photos to `assets/photos/` (Add file → Upload files). Keep them under ~500 KB (about 1800 px wide); ask Claude to resize large camera files. An optional `"thumb"` (about 640 px) loads in the grid, and the full photo opens on tap.
2. Add one line per photo to `photos.json`, for example:
```json
{
  "photos": [
    { "src": "assets/photos/research-day-2026-awards.jpg", "caption": "Award recipients, MRFA Research Day 2026" },
    { "src": "assets/photos/poster-session.jpg", "caption": "Poster session, Kinne Auditorium" }
  ]
}
```
The Photos section appears automatically once the list has at least one photo. Tapping a photo opens it full size.
