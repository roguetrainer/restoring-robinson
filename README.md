# Restoring Robinson

This project aims to restore, transcribe, and re-generate the lectures of economist Joan Robinson (1903–1983) using modern AI audio processing. The goal is to produce high-fidelity audio of her 1974 lectures, which currently exist only as degraded field recordings.

---
![JR](./img/Robinson-TV.png)   
---

For transcripts see [Transcripts](./data/transcripts/) & below.

## Workflows: Commercial vs. Open Source

We support two distinct workflows for this project.

| Feature | Commercial Workflow | Open Source / Hacker Workflow |
| :--- | :--- | :--- |
| **Philosophy** | "Time is money." Focus on ease of use and GUI. | "Code is control." Focus on privacy, cost, and customizability. |
| **Audio Cleaning** | **Adobe Podcast** (Web). excellent artifact removal, but limited control. | **Demucs / OpenVINO** (Local). Uses stem separation to isolate vocals from room noise. |
| **Transcription** | **Gemini 1.5 Pro** (Web). Massive context window allows uploading full 1hr lectures. | **OpenAI Whisper** (Local). Industry standard accuracy, scriptable in Python. |
| **Voice Cloning** | **ElevenLabs** (Web). The gold standard for emotive cloning. Requires 'Creator' subscription. | **Coqui TTS / XTTS** (Local). State-of-the-art open model. Good timbre match, harder to control inflection. |
| **Cost** | Approx. $15 - $30 USD / month. | $0 (Requires GPU: NVIDIA recommended, or Apple Silicon). |

## getting Started

1.  **Download Audio:** Check `docs/found_audio_sources.md` for links.
2.  **Choose your path:**
    * **Commercial:** Follow `docs/commercial_workflow.md`.
    * **Open Source:** Install dependencies and run `notebooks/01_restoration_pipeline.ipynb`.


## Transcripts

For transcripts see [`Transcripts`](./data/transcripts/)
* [Stanford '74](https://www.bobm.net.au/iows/jrobinson.html)
    * [JoanRobinson1.md](./data/transcripts/JoanRobinson1.md)
    * [JoanRobinson2-1.md](./data/transcripts/JoanRobinson2-1.md)
    * [JoanRobinson2-2.md](./data/transcripts/JoanRobinson2-2.md)
    * [JoanRobinson3-1.md](./data/transcripts/JoanRobinson3-1.md)
    * [JoanRobinson3-2.md](./data/transcripts/JoanRobinson3-2.md)
* [Queens '74](https://www.queensu.ca/dunning-trust/joan-v-robinson-1973-1974)
    * [SR181-Robinson_Full_Growth_and_the_Economist](./data/transcripts/SR181-Robinson_Full_Growth_and_the_Economist.md)
    * [SR182-Robinson_Full_Doomsday](./data/transcripts/SR182-Robinson_Full_Doomsday.md)

## Related Repos:
* [`beggar-thy-neighbour`](https://github.com/roguetrainer/beggar-thy-neighbour)