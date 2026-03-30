# ChemAI MLP Demo

Interactive web demo for the [ChemAI Laboratory](https://ilkhamfy.github.io/chemai-website/) at McMaster University. Users submit input through a browser UI and receive predictions from a neural network in real time.

### Architecture

```
Frontend (Astro/JS)  ──REST──▶  Express (Node.js)  ──▶  Python (model + API)
       UI / UX                   middleware / routes       MLP inference
```

### Project Structure

```
frontend/          Astro site — input form, results display, visualizations
backend/
  server.js        Express app — REST endpoints, calls Python scripts
  model.py         MLP / CNN definition and inference
  api.py           Python interface called by Express
  wrapper.py       Utilities, pre/post-processing
```

### Getting Started

**Prerequisites:** Node.js 18+, Python 3.10+

```bash
# Backend
cd backend
pip install -r requirements.txt
node server.js

# Frontend
cd frontend
npm install
npm run dev
```

### Contributors

- **Ilkham Yabbarov** — Frontend, UI/UX
- **Uriel Garcilazo Cruz** — Backend, middleware, model wiring
