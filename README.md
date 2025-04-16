# AI Chat Application

A modern, real-time chat application built with Next.js and OpenAI's GPT models. This application demonstrates advanced AI chat capabilities with a clean, user-friendly interface.

## Features

### Core Features
- 🤖 Real-time AI Chat Interface
- ⚡ Streaming Responses
- 🎯 Context-Aware Conversations
- 🔄 Message History
- 📱 Responsive Design

### Technical Features
- 🚀 Built with Next.js 15
- 🎨 Modern UI with Tailwind CSS
- 🔌 OpenAI Integration
- 🔄 Server-Side Streaming
- 📝 TypeScript Support
- 🛡️ Error Handling & Rate Limiting

## Available Routes

The application includes several specialized chat endpoints:

- `/` - Main chat interface
- `/api/chat` - Core chat API endpoint
- `/api/completion` - Text completion endpoint
- `/api/assistant` - AI assistant endpoint
- `/api/generate-image` - Image generation endpoint
- `/api/files` - File handling endpoint

## Getting Started

### Prerequisites
- Node.js 18+ installed
- OpenAI API key
- npm or yarn package manager

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ai-chat-app.git
   cd ai-chat-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a `.env.local` file in the root directory:
   ```env
   OPENAI_API_KEY=your_api_key_here
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser

## Project Structure

```
ai-chat-app/
├── app/
│   ├── api/           # API routes
│   ├── components/    # React components
│   ├── layout.tsx     # Root layout
│   └── page.tsx       # Home page
├── public/           # Static files
├── styles/          # CSS styles
├── types/           # TypeScript types
└── utils/           # Utility functions
```

## API Routes

### `/api/chat`
Main chat endpoint that handles:
- Real-time message streaming
- Context management
- Error handling
- Rate limiting

Example request:
```typescript
const response = await fetch('/api/chat', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    messages: [{ role: 'user', content: 'Hello!' }]
  })
});
```

### `/api/completion`
Text completion endpoint for single-response queries.

### `/api/generate-image`
Image generation endpoint using DALL-E models.

## Configuration

### Environment Variables
- `OPENAI_API_KEY`: Your OpenAI API key
- `MAX_TOKENS`: Maximum tokens per request (optional)
- `TEMPERATURE`: Response randomness (0-1, optional)

### OpenAI Models
The application supports various OpenAI models:
- GPT-4
- GPT-3.5-turbo
- DALL-E (for image generation)

## Development

### Running Tests
```bash
npm run test
```

### Building for Production
```bash
npm run build
```

### Deployment
The application can be deployed to various platforms:
- Vercel (recommended)
- Netlify
- AWS
- Docker

## Best Practices

### Rate Limiting
The application includes built-in rate limiting to:
- Prevent API abuse
- Manage costs
- Ensure fair usage

### Error Handling
Comprehensive error handling for:
- API failures
- Token limits
- Network issues
- Invalid requests

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please:
1. Check the documentation
2. Open an issue
3. Contact the maintainers

## Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- Powered by [OpenAI](https://openai.com/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
