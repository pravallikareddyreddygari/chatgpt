# Mini ChatGPT

A simple ChatGPT-style interface built with Next.js, React, TypeScript, and Tailwind CSS.

## Features

- Clean, modern UI with dark mode support
- Real-time message streaming
- Responsive design
- API endpoint for AI integration

## Getting Started

1. Install dependencies (already done):
   ```bash
   npm install
   ```

2. Run the development server:
   ```bash
   npm run dev
   ```

3. Open [http://localhost:3000](http://localhost:3000) in your browser

## Usage

Type your question in the input field and press Enter or click Send.

## Integration with Real AI

To connect to a real AI API (like OpenAI's GPT):

1. Update `app/api/chat/route.ts` to use your API key
2. Replace the simulated response with actual API calls

Example OpenAI integration:
```typescript
const response = await fetch("https://api.openai.com/v1/chat/completions", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    "Authorization": `Bearer ${process.env.OPENAI_API_KEY}`,
  },
  body: JSON.stringify({
    model: "gpt-3.5-turbo",
    messages: messages,
  }),
});
```

## Tech Stack

- Next.js 14 (App Router)
- React 18
- TypeScript
- Tailwind CSS
