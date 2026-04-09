# Interview Transcript Organizer

[![中文](https://img.shields.io/badge/lang-中文-red.svg)](README.md)
[![English](https://img.shields.io/badge/lang-English-blue.svg)](README.en.md)

A Claude Code skill that automatically turns raw interview transcripts into well-formatted, structured Word documents.

## Overview

The most painful part of doing interviews isn't recording—it's formatting the transcript. Raw transcripts are usually stuffed with filler words like "uh" and "um", giant walls of text without paragraphs, and a chaotic timeline.

This skill handles all the mechanical layout work for you:
- Auto-group content into themed chapters
- Clean Q&A formatting: interviewer questions in bold blue, responses in black left-aligned
- Semantic paragraphing: split long responses by meaning shifts
- Remove filler words, reconnections, and oral redundancy
- Correct transcription errors and unify terminology
- Output a strictly formatted `.docx` Word document

## Features

| Feature | Description |
|---------|-------------|
| **Thematic chapters** | Split into 4~8 themed chapters with Chinese numerals |
| **Q&A formatting** | Clear distinction between interviewer and respondent |
| **Semantic paragraphing** | Break walls of text into readable, logical paragraphs |
| **Oral cleanup** | Remove filler words, connection checks, and repetition |
| **Transcription correction** | Fix ASR errors, expand abbreviations, unify names |
| **Strict typography** | KaiTi + Times New Roman, chapter headings with gray shading |

## Triggers

After installing this skill in Claude Code, say any of the following:

- "帮我整理这个访谈录音"
- "把这个访谈录音生成 Word 文档"
- "访谈录音整理"
- "录音整理成 Word"
- "梳理问题和回答"

## Format Quick Reference

- **File format**: `.docx`, A4 portrait
- **Fonts**: KaiTi for Chinese, Times New Roman for English/numbers, 10.5 pt body text
- **Main title**: 16 pt, bold, centered
- **Chapter titles**: 14 pt, bold, gray text shading (RGB `D9D9D9`)
- **Interviewer questions**: Bold blue (RGB `0, 112, 192`), prefixed with `【记者】`
- **Respondent answers**: Black, regular weight, prefixed with `【受访者】`, left-aligned, no indent

> See `SKILL.md` for complete formatting rules (in Chinese).

## Installation

1. Copy this folder into your Claude Code skills directory:
   ```bash
   cp -r interview-transcript-organizer ~/.claude/skills/
   ```
2. Restart or reload Claude Code skills.
3. Use the trigger phrases above.

## Usage Example

**User input:**
> 帮我整理这个访谈录音，生成 Word 文档。这是转写文本：[paste transcript]

**Skill workflow:**
1. Extract respondent name, interviewer, and format
2. Split into themed chapters
3. Clean redundancy, correct errors, and paragraph semantically
4. Apply formatting and generate `.docx`
5. Ask for save path and output the file

## License

MIT License — free for commercial or personal use, attribution appreciated.
