# reference-analyzer

Claude Code skill that gives a detailed, professional breakdown of a photo, screenshot, or local video reference — how it was made and how to reproduce it, both for a real shoot and as an AI video/image prompt.

Built as a personal alternative to the "Ідеальний Аналізатор Референсів" custom GPT, adapted for a photo/video production + AI-video workflow.

## Install

Copy `SKILL.md` into `~/.claude/skills/reference-analyzer/` (or clone this repo directly into that path). Claude Code picks up skills from that directory automatically.

## Use

In Claude Code, upload a reference photo/screenshot (1–5 images), or point to a local video file, and ask for an analysis — e.g. "проаналізуй цей референс", "розбери це відео", "зроби мені AI-промт з цього фото". The skill also works invoked explicitly as `/reference-analyzer`.

For video, the skill uses `ffmpeg`/`ffprobe` (must be installed — `brew install ffmpeg` on macOS) to pull key frames and basic metadata before analyzing.

Full behavior, the report structure, and the quality rules live in [`SKILL.md`](./SKILL.md).
