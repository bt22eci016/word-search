# Word Search Live Overlay

A Flask + Socket.IO word-search game overlay for live streams.
It listens to YouTube Live chat messages, validates found words against a dictionary, updates scores, and displays results in a browser overlay.

## Project Structure

- `main.py` — game logic, Flask server, chat integration
- `templates/overlay.html` — overlay UI
- `requirements.txt` — Python dependencies
- `.env.example` — environment variable template

## Setup

1. Create and activate a virtual environment.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Create your env file:

```bash
copy .env.example .env
```

4. Edit `.env` and set at least:

- `VIDEO_ID` (required for live mode)

## Run

### Mock mode (no YouTube required)

```bash
python main.py --mock
```

### Live mode (YouTube chat)

```bash
python main.py
```

### Print one generated round and exit

```bash
python main.py --print-words
```

Overlay URL: `http://localhost:5000`

## Notes

- In live mode, the app exits if `VIDEO_ID` is missing.
- `YOUTUBE_API_KEY` is currently optional and reserved for future use.
