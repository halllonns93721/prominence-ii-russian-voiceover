# Prominence II — Russian Voiceover

![Project logo](assets/logo.png)

Russian AI-assisted voiceover replacing 57 character dialogue recordings in Prominence II: Hasturian Era.

> **Status: documentation repository.** This repo contains documentation, artwork, and reproducible build tooling.
> No audio files are published here. Audio distribution requires the original author's permission
> (see [RIGHTS](#rights--license) and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)).

[Читать на русском](README.ru.md) · **Version:** v1.0.0 · **Game:** Minecraft 1.20.1 (Fabric) · **Modpack:** Prominence II: Hasturian Era v4.1.2

## What this is

A Russian voiceover resource pack for the story dialogues of Prominence II: Hasturian Era:

- **57 dialogue recordings** — 6 characters: Radin (8), S'kellak (23), Gumas (4), Hastur (5), Alm (6), Mirgaff (11)
- **Format:** OGG Vorbis, 48 kHz mono, original file paths and names preserved
- **Pack metadata:** `pack_format` 15 (Minecraft 1.20.1), clean `pack.mcmeta`, custom `pack.png`
- All 57 files decode successfully, map 1:1 to the mod's sound events, and match the original durations within ~1%

## Installation

Full steps: [docs/INSTALLATION.md](docs/INSTALLATION.md).

1. Get the voice-pack ZIP (`Prominence_II_Russian_Voice_Pack_Final.zip`, v1.0.0) from the release channel.
2. Copy it into `minecraft/resourcepacks/`.
3. Enable it at the top of the resource-pack list.
4. Disable other voice packs to avoid overlap.
5. Rollback: disable the pack — the mod JAR restores the original English voices.

## Compatibility

See [docs/COMPATIBILITY.md](docs/COMPATIBILITY.md). Short version: Minecraft 1.20.1 / Fabric,
Prominence II: Hasturian Era v4.1.2, `prominent` namespace, no `sounds.json` override, no music/effects touched.

## Verification

Every released file passed: name/event/path mapping 57/57, FFmpeg decode 57/57, SHA-256 manifest.
Details: [docs/VERIFICATION.md](docs/VERIFICATION.md).

## Rights & license

Unofficial, AI-assisted community localization. **Not the original actors' performance, not an official release.**
Original mod content: Cinderstone Studios / ElocinDev. See [LICENSE](LICENSE) and
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). Public audio distribution requires permission —
do not re-upload the recordings elsewhere without it.
