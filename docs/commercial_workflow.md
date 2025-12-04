# Commercial Tools Workflow

If you prefer using web-based tools for the highest quality with the least configuration.

## Phase 1: Restoration (Adobe Podcast)
1.  Navigate to **Adobe Podcast Enhance**.
2.  Upload the raw MP3 files (limit: 30 mins per file on free tier. You may need to split the MP3s).
3.  Set enhancement strength to ~70% (going to 100% can make the voice sound synthetic).
4.  Download the "Enhanced" WAV file.

## Phase 2: Transcription (Gemini)
1.  Go to **Google AI Studio** (aistudio.google.com).
2.  Select **Gemini 1.5 Pro**.
3.  Click the `+` button and upload your **Enhanced WAV** file.
4.  Prompt: *"Please provide a verbatim transcript of this lecture. Do not summarize. Include timestamps every 5 minutes."*
5.  Save the text as `transcript.txt`.

## Phase 3: Cloning & Generation (ElevenLabs)
*Requirement: Creator Plan (approx $11/mo).*
1.  Go to **VoiceLab** -> **Instant Voice Cloning**.
2.  Upload 5-10 minutes of the *cleanest* enhanced audio from Phase 1.
3.  **Generation Strategy:**
    * **Text-to-Speech:** Paste the transcript into the generation box.
    * **Speech-to-Speech (Recommended):** Record yourself reading the transcript to provide the *inflection* and *pacing*. Upload this as the "Driver" audio.
4.  Download the result.