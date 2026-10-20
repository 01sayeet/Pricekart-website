# PriceKart (live data)

Website + Node.js backend. Prices come live from a RapidAPI product-data API; the chatbot uses Google Gemini.
API keys stay on the server in `.env` and never reach the browser.

## Run
1. Install Node.js 18 or newer.
2. In this folder: `npm install`
3. Copy `.env.example` to `.env` and add your `RAPIDAPI_KEY` and `GEMINI_API_KEY`.
4. `npm start`, then open http://localhost:5000

## Notes
- Subscribe to "Real-Time Product Search" on RapidAPI. If your plan shows different endpoint names, set `SEARCH_PATH` and `OFFERS_PATH` in `.env`.
- Search results are cached for 10 minutes to save your API quota.
- Each search returns `apiMs` (T_api) and `procMs` (T_proc), shown at the bottom of the page. Use them for the paper's response-time graph.
