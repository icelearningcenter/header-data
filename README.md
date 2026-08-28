# header-data

HTML fragments embedded in the video-navigation pages of the three ICE sites,
served from GitHub Pages at **https://icelearningcenter.github.io/header-data/**.

## Most of this repo is generated — do not hand-edit it

Nine of the eleven content files are **rebuilt and force-pushed daily at 07:00
UTC** by `Update Content` in
[`brightcove-tools`](https://github.com/icelearningcenter/brightcove-tools/blob/main/.github/workflows/update-content.yml).
An edit made here is silently overwritten on the next run, with no warning and
no failed build. Fix the *source*, not the file.

| File | Generated? | Built from | Change it by |
|---|---|---|---|
| `icelearningcenter-titles.html` | yes | Brightcove playlists + videos | editing Brightcove |
| `icevideolibrary-titles.html` | yes | Brightcove | editing Brightcove |
| `videocourses-titles.html` | yes | Brightcove | editing Brightcove |
| `icelearningcenter-keywords.html` | yes | Brightcove video keywords | editing Brightcove |
| `icevideolibrary-keywords.html` | yes | Brightcove | editing Brightcove |
| `videocourses-keywords.html` | yes | Brightcove | editing Brightcove |
| `icelearningcenter-clients.html` | yes | the client Google Sheet | editing the Sheet |
| `icevideolibrary-clients.html` | yes | the client Google Sheet | editing the Sheet |
| `videocourses-clients.html` | yes | the client Google Sheet | editing the Sheet |
| `icelearningcenter-practice.html` | **no** | — | editing it here |
| `videocourses-practice.html` | **no** | — | editing it here |

The two `*-practice.html` files are the only ones maintained by hand. They are
safe to edit directly, and nothing regenerates them.

The client Google Sheet is the one read by
`brightcove-tools/scripts/generate_client_content.py`; a client only appears in
a `*-clients.html` table when its `Status` column reads `Active`.

## The three site variants

Each content kind exists once per catalogue, because the three sites show
different subsets of the same Brightcove library:

- `icelearningcenter-*` — the combined ICE Video Library & Video Courses view
- `icevideolibrary-*` — ICE Video Library only
- `videocourses-*` — StrokeHelp Video Courses only

## Related

- [`client-data`](https://github.com/icelearningcenter/client-data) — the client
  record pages these `*-clients.html` tables link into, plus the generated
  `client-list.js` index.
- [`brightcove-tools`](https://github.com/icelearningcenter/brightcove-tools) —
  the generator, the schedule, and the Brightcove and Sheets credentials.
