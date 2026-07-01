# embeddings-explorer

Visualize text embeddings in 2D. See how sentences cluster in vector space.

Embeddings are vectors representing semantic meaning — similar sentences should be close together. This uses PCA to project high-dimensional vectors down to 2D so you can see the relationships.

## What to explore

- Do synonyms land near each other? ("car" vs "automobile")
- Do topic clusters form? (cooking sentences vs programming sentences)
- Where do ambiguous words land? ("bank" the institution vs "bank" of a river)

## Features

- Paste sentences (one per line) or use built-in example sets
- Interactive 2D scatter plot — hover to read each sentence
- Color-code by group
- Cosine similarity matrix table

## Setup

```bash
npm install
cp .env.example .env  # needs OpenAI API key for embeddings
npm run dev
```

## Notes

Uses `text-embedding-3-small` — cheap and good enough for visualization. Each batch of sentences is one API call.
