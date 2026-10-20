# myTunes — Personal Music App (starter MVP)

A responsive, Apple Music-inspired personal music player prototype.

## Run it
1. Unzip the project.
2. Open `index.html` in a modern browser (Chrome, Edge, Firefox or Safari).
3. Click **Add music** and choose audio files from your device.
4. Play songs, seek, skip tracks, like songs, search, and create playlists.

No installation, API key, server, or payment is needed for this prototype.

## Important current limitations
- Audio files are selected from your device and played in the current browser session. They are **not uploaded to cloud storage** yet.
- Browsers cannot keep a selected local file's temporary playback URL working forever; reselect files after a reload.
- Playlist names are saved in browser local storage, but the prototype does not yet synchronize songs or playlists across devices.
- Song metadata is initially derived from the filename. Editing artist/album metadata is a planned next step.
- This is a front-end prototype, not yet a deployed website.

## Next milestone: cloud version
We will connect a Supabase project:
- Supabase Auth for private user accounts.
- Supabase Storage for the user's audio files and cover art.
- A Postgres database for track metadata, likes, playlists, and playlist membership.
- Private storage policies and short-lived signed URLs so files are not publicly accessible.

Before uploading, use audio files you own or have permission to store and stream. Review the current provider free-tier limits before committing to a library size.


Album artwork: embedded ID3 cover art is read from MP3 files when available. Formats that do not expose supported embedded artwork will use generated placeholder art.
