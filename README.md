# engraid
An interactive English vocabulary puzzle game web app combining classic Sudoku mechanics with word learning.  Vocabdoku - An interactive English vocabulary puzzle and word learning web game.

## AI Tutor chat (OmniRoute)

The game includes an **AI Tutor** chat (button at the bottom right). It talks to an
[OmniRoute](https://github.com/cheaper-inference/OmniRoute) gateway through its
OpenAI-compatible `/v1/chat/completions` endpoint, with streaming replies. The tutor
knows the current level's word list and the word shown in the Word Inspector.

1. Start OmniRoute (`npx omniroute`), open its dashboard at `http://localhost:20128`,
   connect at least one provider, and create an API key.
2. If the game is served from a website (not opened as a local file), allow that site
   in OmniRoute's CORS settings, e.g. `CORS_ALLOWED_ORIGINS=https://your-game.example.com`.
3. In the game, open **AI Tutor → ⚙️** and enter the OmniRoute URL
   (default `http://localhost:20128/v1`), your API key, and a model (default `auto`).

Settings and chat history are kept in the browser's `localStorage`. The API key is stored
there in plain text, so only use this on a device you trust.
