#  Pixie Chatbot 

## What is Pixie?
A pixel art themed AI chatbot built with HTML, CSS and React, powered by Groq's free AI API. Pixie is a magical, cheerful, and slightly dumb AI assistant with a Soft Gameboy aesthetic.

---

## Tech Stack
- **React** (via unpkg/supersimpledev)
- **Groq API** — free AI API (`llama-3.1-8b-instant` model)
- **Pixelify Sans** — pixel art font
- **Pixel art GIF** — background image

---

## What You Learned

### React
- How components work (`App`, `ChatMessages`, `Chatmessage`, `Chatinput`)
- Props — passing data between components
- State — `React.useState()` for messages and input text
- `useRef` + `useEffect` for auto-scrolling
- `className` instead of `class` in JSX

### JavaScript
- `async/await` — waiting for slow API responses
- `fetch()` — making API calls
- `.map()` — transforming arrays
- `crypto.randomUUID()` — generating unique IDs
- Error handling with `response.ok`


### CSS
- CSS variables (`--gb-lightest`, `--gb-dark` etc.)
- Pixel art button using `box-shadow` layers
- Translucent containers with `rgba()` and `backdrop-filter`
- Full screen background with `background-size: cover`
- Flexbox layout — pushing input to bottom with `flex-grow: 1`
- `calc(100vh - 40px)` for full height with spacing

---


## How to Run
1. Get a free Groq key from [console.groq.com](https://console.groq.com)
2. Paste it in `chatbot.html` where it says `YOUR_GROQ_KEY_HERE`
3. Open `chatbot.html` in your browser

---

## Groq API Format
```javascript
const response = await fetch('https://api.groq.com/openai/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer YOUR_GROQ_KEY_HERE'
  },
  body: JSON.stringify({
    model: 'llama-3.1-8b-instant',
    messages: [
      { role: 'system', content: 'You are Pixie...' },
      ...chatHistory
    ]
  })
});
const data = await response.json();
const reply = data.choices[0].message.content;
```
---

*Built with pixel magic*
