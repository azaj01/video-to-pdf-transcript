
# Avatar Training Suite - Video to PDF Transcript

Convert videos to structured PDF transcripts for AI Avatar training and Vector Database (RAG) indexing.

## Features

- 🎥 **Video Processing**: Extract transcripts from video files
- 🆓 **Free Transcription**: Uses Whisper.js (browser-based, unlimited, free)
- 💰 **Low Cost**: Only uses Gemini API for metadata (cheap text processing)
- 📄 **Multiple Export Formats**: PDF, JSON, TXT, CSV
- 🌍 **Multi-language Support**: Handles code-switching and multiple languages
- ⚡ **Browser-Based**: No server required - everything runs in your browser

## Run Locally

**Prerequisites:** Node.js

1. Install dependencies:
   ```bash
   npm install
   ```

2. Set the `GEMINI_API_KEY` in `.env.local` to your Gemini API key:
   ```
   GEMINI_API_KEY=your_api_key_here
   ```

3. Run the app:
   ```bash
   npm run dev
   ```

4. Open `http://localhost:3000` in your browser

**That's it!** No server needed - everything runs in your browser.

## How It Works

1. **Audio Extraction**: Uses FFmpeg.wasm to extract audio from video (browser-based)
2. **Free Transcription**: Uses Whisper.js for unlimited free transcription (browser-based)
3. **Metadata Enrichment**: Uses Gemini API for cheap text-based metadata extraction
4. **Export**: Generate PDF, JSON, TXT, or CSV files

## Cost Breakdown

- **Transcription**: FREE (Whisper.js in browser)
- **Metadata**: ~$0.01 per 2-hour video (Gemini API for text only)
- **Total**: ~$0.01 per video (vs ~$9.00 with full Gemini video processing)

## Deployment

### Vercel (Recommended)

1. Push to GitHub
2. Connect to Vercel
3. Add `GEMINI_API_KEY` in Vercel environment variables
4. Deploy!

The app works as a static site - no serverless functions needed for the free transcription approach.

## Tech Stack

- **Frontend**: React + TypeScript + Vite
- **Transcription**: Whisper.js (@xenova/transformers)
- **Audio Processing**: FFmpeg.wasm
- **Metadata**: Google Gemini API
- **PDF Generation**: jsPDF

## Notes

- First-time use: Whisper model (~75MB) downloads automatically and is cached
- Processing speed: ~1x real-time (normal for free browser-based transcription)
- File size limit: 2GB (browser limitation)
- Works offline: After initial model download, transcription works offline
