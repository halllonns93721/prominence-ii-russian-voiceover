# Compatibility

- **Game:** Minecraft 1.20.1 (Java, Fabric Loader). `pack_format` 15.
- **Modpack:** Prominence II: Hasturian Era v4.1.2.
- **Namespace:** `assets/prominent/sounds/dialogue/...` — identical paths and filenames
  to the mod's originals, so the mod's own `sounds.json` events resolve without any override.
- **Audio:** 57 × OGG Vorbis, 48 kHz mono.
- **Untouched:** music, sound effects, quests, saves, configs, mod JARs.
- **Known approximation:** the mod's English originals use mixed specs (44.1/48 kHz,
  mono/stereo); the Russian pack standardizes on 48 kHz mono. This is valid for
  `stream:true` voice events and needs no `sounds.json` change.
- **Subtitles:** spoken lines match the project's Russian subtitle companion
  (104 dialogue keys); quest translations from other packs are a separate concern.
