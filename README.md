# Gemini Search

A Perplexity-style search engine powered by Google's Gemini 2.0 Flash model with grounding through Google Search. Get AI-powered answers to your questions with real-time web sources and citations.

Created by [@ammaar](https://x.com/ammaar)

![Kapture 2025-01-04 at 14 35 14](https://github.com/user-attachments/assets/2302898e-03ae-40a6-a16c-301d6b91c5af)


## Features

- 🔍 Real-time web search integration
- 🤖 Powered by Google's latest Gemini 2.0 Flash model
- 📚 Source citations and references for answers
- 💬 Follow-up questions in the same chat session
- 🎨 Clean, modern UI inspired by Perplexity
- ⚡ Fast response times

## Tech Stack

- Frontend: React + Vite + TypeScript + Tailwind CSS
- Backend: Express.js + TypeScript
- AI: Google Gemini 2.0 Flash API
- Search: Google Search API integration

## Setup

### Prerequisites

- Node.js (v18 or higher recommended)
- npm or yarn
- A Google API key with access to Gemini API

### Installation

#### With npm

1. Clone the repository:

   ```bash
   git clone https://github.com/ammaarreshi/Gemini-Search.git
   cd Gemini-Search
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory:

   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

#### Docker Usage

##### Pull from GitHub Container Registry

```bash
# Pull the image
docker pull ghcr.io/curtaintears/gemini-search:latest

# Run with default port (7788)
docker run -d \
  -p 7788:7788 \
  -e GOOGLE_API_KEY=your_api_key_here \
  --name gemini-search \
  ghcr.io/curtaintears/gemini-search:latest

# Run with custom port
docker run -d \
  -p 3000:3000 \
  -e PORT=3000 \
  -e GOOGLE_API_KEY=your_api_key_here \
  --name gemini-search \
  ghcr.io/curtaintears/gemini-search:latest
```

##### Build and Run Locally

```bash
# Build the image
docker build -t gemini-search .

# Run with default port (7788)
docker run -d \
  -p 7788:7788 \
  -e GOOGLE_API_KEY=your_api_key_here \
  --name gemini-search \
  gemini-search

# Run with custom port
docker run -d \
  -p 3000:3000 \
  -e PORT=3000 \
  -e GOOGLE_API_KEY=your_api_key_here \
  --name gemini-search \
  gemini-search
```

##### Environment Variables

- `PORT`: Application port (default: 7788)
- `GOOGLE_API_KEY`:Your API Key

##### Architecture Support

The Docker image supports both AMD64 (x86-64) and ARM64 architectures, making it compatible with:
- Traditional Intel/AMD processors
- Apple Silicon (M1/M2) Macs
- ARM-based servers


## Development | 开发

[Development instructions to be added... | 开发指南待添加...]

## License | 许可证

[Your License | 你的许可证]

## Environment Variables

- `GOOGLE_API_KEY`: Your Google API key with access to Gemini API
- `NODE_ENV`: Set to "development" by default, use "production" for production builds
- `PORT`: Server port (defaults to 3000)

## Development

- `npm run dev`: Start the development server
- `npm run build`: Build for production
- `npm run start`: Run the production server
- `npm run check`: Run TypeScript type checking

## Security Notes

- Never commit your `.env` file or expose your API keys
- The `.gitignore` file is configured to exclude sensitive files
- If you fork this repository, make sure to use your own API keys

## License

MIT License - feel free to use this code for your own projects!

## Acknowledgments

- Inspired by [Perplexity](https://www.perplexity.ai/)
- Built with [Google's Gemini API](https://ai.google.dev/)
- UI components from [shadcn/ui](https://ui.shadcn.com/)
