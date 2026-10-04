# Crypto Dashboard

A simple web page that tracks your crypto. Add the coins you own and how much of each, and it shows:

- Your total portfolio value, updated every minute
- How much it moved in the last 24 hours
- Gain or loss on each coin, if you enter what you paid
- A 7-day price line, 24-hour change and market cap for each coin
- A chart of how your portfolio is split between coins

It is one file (`index.html`). There is nothing to install and no server to run.

## How to use it

1. Open the page.
2. In **Add a coin**, search for a coin (or tap a quick-add button like BTC).
3. Enter how much you own. Optionally enter the total you paid in US dollars, which turns on gain/loss.
4. Click **Add**.

Click the pencil on any row to change the amount or remove the coin. Click a column heading to sort.

## Your data stays private

Your holdings are saved **only in your own browser** (local storage). They are never sent anywhere and are not stored in this repository, so it is safe to keep the repo public.

Because of that, the page will not show the same holdings on a different device or browser. Use **Backup** to download your holdings as a file, and **Restore** to load them somewhere else.

## Where the prices come from

Prices come from the free [CoinGecko](https://www.coingecko.com) API. No account or key is needed. If CoinGecko is busy or you are offline, the page shows the last saved prices and a message at the top.

## Put it online (Cloudflare Pages)

1. In Cloudflare, go to **Workers & Pages**, then **Create**, then **Pages**, then **Connect to Git**.
2. Pick the `ltiam/stonks` repository.
3. Set **Framework preset** to `None`, leave **Build command** empty, and set **Build output directory** to `/`.
4. Click **Save and Deploy**.

After that, every push to `main` updates the live site automatically.

GitHub Pages also works: in the repo, go to **Settings**, then **Pages**, then deploy from the `main` branch and the `/ (root)` folder.

## Not financial advice

This is a personal tracking tool. Prices can be delayed or wrong. Do not make financial decisions based only on this page.
