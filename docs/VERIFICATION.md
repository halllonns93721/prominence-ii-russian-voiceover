# Verification summary (v1.0.0)

Audit performed locally on the 57 source files before assembly. Method: filename/event/path
mapping against the mod's sound registry, SHA-256 checksums, FFmpeg full decode, audio
level/duration analysis, and spot ASR language checks.

- **Files found:** 57 `.ogg`, flat folder, no subdirectories.
- **Name/event/path mapping:** 57/57 match the expected set — missing 0, extra 0, duplicate
  filenames 0, duplicate content 0.
- **Container repair:** 56 files arrived as Theora-video + Vorbis-audio multiplexes
  (export artifact; video frame carries a dubbing-tool watermark) and 1 as pure Vorbis.
  Video tracks were removed with stream copy (`-map 0:a -c:a copy`); decoded PCM is
  SHA-identical to the sources for 57/57 — no regeneration, no re-encoding.
- **Decode:** FFmpeg 57/57 PASS; secondary decoder read 57/57 (codec Ogg/Vorbis everywhere).
- **Silence/clipping/truncation:** 0 near-silent, 0 clipped peaks, 0 empty.
- **Durations vs English originals:** worst deltas ≈ ±1% (duration-matched dubbing).
- **Speech content:** ASR spot-check on 6 files (one per character) detected Russian with
  probability 1.00 and transcripts matching the expected lines. ASR confirms language
  presence, not acting quality.
- **Pack validation:** final ZIP opens, CRC clean, 59 entries (57 OGG + `pack.mcmeta` +
  `pack.png`), no junk; all 57 OGG bytes re-decoded from inside the ZIP successfully.

Full per-file hashes, measurements, and reconciliation decisions are kept with the
maintainer's audit archive; this file is the public summary. Listening QA (stress,
acting, voice identity) is a separate human process and is not claimed here.
