# Set Your Language

Before using GtV for streaming playback, set your preferred audio language in the Dynamic Library plugin.

## Setup

1. Open the Jellyfin Dashboard.
2. Go to **Plugins**.
3. Open **Dynamic Library**.
4. Find the preferred audio/language setting.
5. Set it to your preferred language, for example **English**.
6. Save the settings.
7. Restart Jellyfin if prompted.

## Why this matters

Some AIOStreams sources contain multiple audio tracks, such as Polish + English or Italian + English. Many files mark the non-English track as the container default.

Dynamic Library's language preference is currently the reliable way to make Jellyfin start a compatible multi-audio source in your chosen language.

Example:

```text
Preferred Language: English
```

If your preferred language is available in the selected source, playback should start in that language. If it is not available, playback falls back to an available track.

## Current GtV status

- First-load AIOStreams source/version picker is working.
- Dynamic Library selected-source ffprobe probing is working.
- Real audio stream metadata is reaching GtV.
- Manual in-player audio switching is still under investigation.
- Until that is resolved, configure your preferred language in Dynamic Library before playback.
