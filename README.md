# music-kanazawa-it-club

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

[
![GitHub Pages](https://img.shields.io/badge/demo-online-blue.svg)
](https://code4fukui.github.io/music-kanazawa-it-club/)

A web-based music player for the "金沢IT部活" (Kanazawa IT Club) playlist, featuring AI-generated music from Suno. This project is a standalone single-page application, easily hosted on services like GitHub Pages.

The player displays a three-column layout against a blurred background that dynamically updates to match the current track's album art:
1.  **Playlist:** A scrollable list of all tracks in the album.
2.  **Player:** The current track's album art, audio controls, and metadata.
3.  **Lyrics:** The full lyrics for the currently playing song.

## Features

-   **Dynamic Background:** Album art is used to create an immersive, blurred background for the player.
-   **Rich Metadata Display:** Shows song title, AI generation prompts, tags, and full lyrics.
-   **Advanced Playback Control:** Implements custom sorting logic, including `riffleShuffle` and a function to prioritize "liked" songs.
-   **Media Session API Integration:** Allows control of playback (play/pause, next/previous, seek) from the operating system's UI, such as the lock screen, notification center, or connected hardware (e.g., headphones, car stereos).
-   **Standalone and Simple:** Runs entirely in the browser with no server-side backend required.

## How to Use Your Own Suno Playlist

This player is configured to use local audio and image files for reliable hosting. To adapt it for your own Suno playlist:

1.  **Get Playlist Data:** On your Suno playlist page, use your browser's developer tools to find and save the playlist's JSON data (see `playlist_org.json` for an example).
2.  **Download Assets:** Download all the `.mp3` audio files and `.jpeg` image files listed in the JSON data.
3.  **Organize Files:** Place the downloaded files into `audio/`, `image/`, and `image_large/` directories.
4.  **Update Playlist:** Create a `playlist.json` file. In it, modify the `audio_url`, `image_url`, and `image_large_url` paths for each track to point to your local files (e.g., `"audio/your-song-id.mp3"`).
5.  **Deploy:** Commit your changes and host the repository on a web server or using GitHub Pages.

## Data and Credits

-   **Music Source:** All music was generated using [Suno AI](https://suno.com/).
-   **Original Playlist:** [金沢IT部活](https://suno.