
# Avatar Training Suite - Video to PDF Transcript

Convert videos to structured PDF transcripts for AI Avatar training and Vector Database (RAG) indexing.

## 🚀 Features

- **Multi-Language Support**: Verbatim transcription in original languages (no translation)
- **AI-Powered Analysis**: Uses Google Gemini 3 Flash for intelligent video processing
- **Multiple Export Formats**: PDF, JSON, TXT, CSV
- **Granular Transcripts**: Sentence-level segmentation with timestamps
- **Tone & Intent Analysis**: Emotional state and functional purpose detection
- **RAG-Ready**: Optimized metadata for Vector Database indexing

## 📋 Tech Stack

- **Frontend**: React 19.2 + TypeScript
- **Build Tool**: Vite 6.2
- **AI**: Google Gemini API
- **Styling**: TailwindCSS + Custom CSS
- **Icons**: Lucide React
- **PDF Generation**: jsPDF + AutoTable

## 🏗️ Architecture

This project follows a **feature-based modular architecture**:

```
src/
├── App.tsx                 # Main application (100 lines)
├── config/                 # Configuration & constants
├── hooks/                  # Custom React hooks
├── components/
│   ├── ui/                # Shared UI components
│   └── features/          # Feature-specific components
├── services/              # External API integrations
├── utils/                 # Helper functions
└── types/                 # TypeScript definitions
```

See [REFACTORING.md](./REFACTORING.md) for detailed architecture documentation.

## 🎯 Quick Start

### Prerequisites
- Node.js 18+
- Google Gemini API key ([Get one here](https://aistudio.google.com/apikey))

### Installation

```bash
# Clone the repository
git clone https://github.com/drdhavaltrivedi/video-to-pdf-transcript.git
cd video-to-pdf-transcript

# Install dependencies
npm install

# Create environment file
echo "GEMINI_API_KEY=your_api_key_here" > .env.local

# Start development server
npm run dev
```

Visit `http://localhost:3000`

## 📝 Usage

1. **Upload Video**: Select an MP4/MOV file (up to 50MB)
2. **Configure**: Add title, speaker name, and category
3. **Process**: Click "Analyze Dataset" and wait 30-90 seconds
4. **Export**: Download as PDF, JSON, TXT, or CSV

## 🔧 Configuration

Edit `src/config/constants.ts` to customize:

- Maximum file size
- Processing timeouts
- Export formats
- UI animation delays
- Error messages

## 📦 Build

```bash
# Production build
npm run build

# Preview production build
npm run preview
```

## 🧪 Key Components

### Custom Hooks
- `useVideoUpload`: File validation and preview management
- `useVideoProcessing`: AI processing workflow orchestration
- `useExport`: Multi-format export functionality

### Features
- **VideoUploadSection**: File picker + metadata form
- **ResultsSummary**: Metadata display + export controls
- **TranscriptView**: Timeline of verbatim segments
- **ProcessingOverlay**: Loading states with progress indicators

## 🔐 Security

- Videos are processed client-side (base64 encoding)
- API keys stored in environment variables only
- Content Security Policy enforced
- No video data persisted on servers

## 🌍 Multi-Language Support

The system preserves **verbatim** content across languages:
- Detects code-switching mid-conversation
- No automatic translation
- Supports 100+ languages via Gemini AI

## 🎨 Customization

The UI uses a modern dark theme with:
- Inter font family
- Slate color palette
- Smooth animations
- Glassmorphism effects

Customize in `index.css` and component styles.

## 📊 Export Formats

| Format | Use Case | Size |
|--------|----------|------|
| **PDF** | Human reading, presentations | Medium |
| **JSON** | API integration, RAG indexing | Small |
| **TXT** | Simple text processing | Small |
| **CSV** | Spreadsheet analysis | Small |

## 🛠️ Development

```bash
# Auto-format code
npm run format

# Type check
npm run type-check

# Lint
npm run lint
```

## 📄 License

MIT License - See LICENSE file

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/drdhavaltrivedi/video-to-pdf-transcript/issues)
- **Docs**: See [REFACTORING.md](./REFACTORING.md)

## 🎯 Roadmap

- [ ] Batch processing
- [ ] Real-time progress tracking
- [ ] Custom PDF templates
- [ ] Speaker diarization improvements
- [ ] Cloud storage integration

---

**Built with ❤️ using React, TypeScript, and Google Gemini AI**
