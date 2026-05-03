# Jauck - Joke Generator 😂

A modern, interactive joke generator built with React, TypeScript, and Tailwind CSS. Fetches random jokes from the Official Joke API and displays them with a beautiful, responsive UI.

## Features ✨

- 🎭 **Multiple Joke Categories**: General, Programming, and Knock-Knock jokes
- 🔄 **Random Joke Generation**: Fetches jokes from the Official Joke API
- 📋 **Copy to Clipboard**: Easily share jokes with friends
- 🌙 **Dark Mode Support**: Beautiful dark theme included
- 🎨 **Modern UI**: Built with Tailwind CSS for a sleek design
- ⚡ **Fast & Responsive**: Optimized performance with Vite
- 🧪 **TypeScript**: Fully typed for better development experience

## Tech Stack 🛠️

- **React 18** - UI Framework
- **TypeScript** - Type Safety
- **Tailwind CSS** - Styling
- **Vite** - Build Tool & Dev Server
- **Lucide React** - Icons
- **Official Joke API** - Joke Data Source

## Project Structure 📁

```
Jauck/
├── public/
│   └── index.html          # HTML Entry Point
├── src/
│   ├── components/
│   │   ├── JokeGenerator.tsx         # Basic Joke Generator
│   │   └── AdvancedJokeGenerator.tsx # Category-based Generator
│   ├── hooks/
│   │   └── useJoke.ts      # Custom Hook for Joke Logic
│   ├── styles/
│   │   └── index.css       # Global Styles & Tailwind Config
│   └── main.tsx            # React App Entry Point
├── package.json            # Dependencies
├── vite.config.ts          # Vite Configuration
├── tsconfig.json           # TypeScript Configuration
└── README.md               # This File
```

## Getting Started 🚀

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Installation

1. **Clone the Repository**
```bash
git clone https://github.com/4gg7s8r56r-star/Jauck.git
cd Jauck
```

2. **Install Dependencies**
```bash
npm install
```

3. **Start Development Server**
```bash
npm run dev
```

The application will open at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

Output will be in the `dist/` directory.

### Preview Production Build

```bash
npm run preview
```

## Usage 📖

### Basic Joke Generator

```tsx
import JokeGenerator from './components/JokeGenerator';

function App() {
  return <JokeGenerator />;
}
```

### Advanced Joke Generator (with Categories)

```tsx
import AdvancedJokeGenerator from './components/AdvancedJokeGenerator';

function App() {
  return <AdvancedJokeGenerator />;
}
```

### Custom Hook Usage

```tsx
import { useJoke } from './hooks/useJoke';

function MyComponent() {
  const { joke, loading, error, fetchJoke, copied, copyToClipboard } = useJoke();
  
  return (
    <div>
      <button onClick={() => fetchJoke('general')}>Get Joke</button>
      <button onClick={copyToClipboard}>{copied ? 'Copied!' : 'Copy'}</button>
      {joke && <p>{joke.joke}</p>}
    </div>
  );
}
```

## API Reference 🔗

### Official Joke API

- **Random Joke**: `https://official-joke-api.appspot.com/random_joke`
- **General Jokes**: `https://official-joke-api.appspot.com/jokes/general/random`
- **Programming Jokes**: `https://official-joke-api.appspot.com/jokes/programming/random`
- **Knock-Knock Jokes**: `https://official-joke-api.appspot.com/jokes/knockknock/random`

## Components 🧩

### JokeGenerator
- Simple, straightforward joke generator
- Auto-fetches random jokes
- Copy to clipboard functionality
- Loading and error states

### AdvancedJokeGenerator
- Category selection (General, Programming, Knock-Knock)
- Enhanced UI with category badges
- Same copy functionality as basic generator
- Better user experience

### useJoke Hook
- Reusable logic for joke fetching
- Error handling
- Copy to clipboard utility
- TypeScript support

## Styling 🎨

The project uses:
- **Tailwind CSS** for utility classes
- **CSS Custom Properties** for theming
- **Dark Mode** via `.dark` class
- **Responsive Design** with mobile-first approach

## Color Scheme 🎯

- **Primary**: `#1F3A5F` (Deep Blue)
- **Accent Orange**: `#E8651E` (Vibrant Orange)
- **Background**: Light & Dark modes supported
- **Border**: Subtle neutral tones

## Performance ⚡

- Lazy loading with code splitting
- Optimized bundle size
- Fast refresh with HMR
- Production build optimizations

## Browser Support 🌐

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing 🤝

Contributions are welcome! Feel free to:
- Report issues
- Submit pull requests
- Suggest improvements

## License 📄

This project is open source and available under the MIT License.

## Author 👨‍💻

Created by [4gg7s8r56r-star](https://github.com/4gg7s8r56r-star)

## Acknowledgments 🙏

- [Official Joke API](https://official-joke-api.appspot.com) for the joke data
- [React](https://react.dev) for the amazing framework
- [Tailwind CSS](https://tailwindcss.com) for the styling utility
- [Vite](https://vitejs.dev) for the blazing fast build tool

---

**Enjoy the laughs! 😂**
