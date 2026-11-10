# Blackjack Book

A real-card blackjack scorekeeper. GitHub Pages serves `docs`; Cloudflare Workers with SQLite-backed Durable Objects stores and serializes each shared game. Configure the API URL in `docs/index.html` and `docs/join/index.html` after deploying the Worker. The host records each result; the dealer pays a 1:1 win or 3:2 blackjack, receives a loss, and pushes transfer nothing. Accounts and monetary transactions are not involved.

Deploy the Worker on Cloudflare's free plan with `npx wrangler deploy`. Configure GitHub Pages to publish the `docs` directory and set its custom domain to `blackjack.zw08.co.uk`. Add the DNS record for the subdomain as instructed by GitHub. Host tokens remain in browser storage; users should not clear it during a game. Free-tier request and storage limits apply.
