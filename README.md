# Terputer: Cannabis Chemical Diversity Census

Source-grounded study package for estimating the size and boundaries of a terpene/terpenoid identity catalog. The local notebook audits frozen census reports; it does not query BigQuery or reconstruct the underlying molecular union.

## Run

`python -m pip install -r requirements.txt` then `jupyter lab notebooks/analysis.ipynb`.

## Current evidence

The report records a 268,924-identity union from source-declared COCONUT and TeroKit candidate sets, with 75,664 identities overlapping. This is not a Terpedia-wide or independently validated terpene count. See whitepaper and report caveats.


## Terpedia access

The optional client in `src/terpedia_access.py` calls the Terpedia Knowledge API at `/v1/tabular/search`. It reads `TERPEDIA_KNOWLEDGE_API_KEY` and `TERPEDIA_KB_API_URL` from the process environment and sends the key in the `x-knowledge-key` header. Copy `.env.example` as a configuration reference, then provide the real key through a local secret manager, Codespaces secret, or authorized GitHub Actions secret. Never commit `.env` or print the key in notebook output.
