# Liltbox

[English](README.md) · [简体中文](README.zh-CN.md)

Liltbox is a free macOS app that turns recordings into readable conversations, short summaries, and a local Markdown library. Record an idea or import audio, then organize it on your Mac. AI agents that can read local files can use the resulting library too.

**Public downloads are being prepared.** The current build is an early development version. Developer ID signing, Apple notarization, and testing on a separate fresh Mac are still pending. No installer is published here yet. Future downloads and release notes will appear in [Releases](https://github.com/rainbowroy/liltbox/releases).

## Features

- **Record or import audio.** Supports M4A, MP3, WAV, WebM, MP4, OGG, and FLAC imports.
- **Organize conversations.** Keep the original transcript alongside a cleaned dialogue, a title, a brief description, and a short summary with transcript references.
- **Review and correct.** Edit transcripts, rename or merge speaker labels, review revision history, and retry organization or summarization.
- **Process locally.** Transcription, speaker labeling, and summarization run on your Mac. After downloading the models, processing works offline.
- **Save readable Markdown.** Keep your library in a folder you choose. Agents with local file access can start from `INDEX.md`; Liltbox does not need to be running.
- **Use Chinese or English.** The interface and Mac menus follow your macOS language settings. Changing the interface language does not translate your recordings or generated content.

## System requirements

| Item | Current target |
| --- | --- |
| Mac | Apple Silicon |
| macOS | 26 or later |
| Memory | 16 GB or more |
| Internet | Required for initial model downloads; processing can then run offline |
| Models | About 2.26 GB, downloaded separately in the app |

The current build has been tested on an M4 Pro Mac with 24 GB of memory. Testing on 16 GB devices and a separate fresh Mac is still pending. Python, Homebrew, and Chrome are not required for users.

## Getting started

These steps describe the current app workflow; a public installer is not yet available.

1. Open Liltbox and choose a folder for your Markdown library.
2. In **Models & storage**, download the transcription, speaker, and organization models. Downloads start only when you choose them.
3. Create a session and start microphone recording, or import an audio file.
4. Save the audio and select **Organize conversation**. The original transcript is saved before the cleaned dialogue and summary are generated.
5. Review the result. Open the library folder to read your Markdown files or let an agent with local file access read them.

Keep your Mac awake with the lid open while recording. If recording is interrupted, use **Recover saved audio** to save the available fragments.

## Your library and privacy

Recordings, transcripts, and summaries are processed and stored locally. The Markdown library contains an `INDEX.md`, session documents, and revision history. Back up the whole library folder to preserve its text and history.

Audio, downloaded models, and task state are stored separately in `~/Library/Application Support/Huiyi/`. To back these up, quit the app first and copy that folder too.

If you give a cloud AI agent access to the library, that agent may send its contents to its service provider. Review your agent's settings before sharing private material.

Transcription and summaries can contain errors. Check important details against the original recording. Speaker labels do not verify a person's identity, and recognition quality for natural multi-speaker meetings is still being evaluated. Make text corrections in the app so the library's archive stays consistent.

## Feedback and community

- [Report a bug](https://github.com/rainbowroy/liltbox/issues/new): include your app version, macOS version, Mac model, steps to reproduce, and expected behavior.
- [Request a feature](https://github.com/rainbowroy/liltbox/issues): describe what you want to accomplish and where the current workflow falls short.
- [Ask questions or share ideas](https://github.com/rainbowroy/liltbox/discussions): Chinese and English are both welcome.

Please remove private recordings, transcript content, and other personal information from public reports and screenshots.

This repository contains product information, downloads when available, and community feedback. Application source code is maintained separately in a private repository.
