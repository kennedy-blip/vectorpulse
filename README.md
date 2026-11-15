# VectorPulse

Full-stack semantic retrieval workbench using Vite, React, TypeScript, Tailwind CSS v4, and Vercel Serverless Functions.

Install with npm install and run npm run dev. Use npx vercel dev to run API routes locally. Import into Vercel using the Vite preset, build command npm run build, and output directory dist.

API: GET /api/ingest lists the index; POST /api/ingest accepts title, content, chunkSize and overlap; DELETE /api/ingest clears the store; POST /api/search accepts query, topK and minScore.

The in-memory store is ephemeral across serverless instances and restarts. Use a persistent database/vector service for production. Embeddings are deterministic 128-dimensional feature hashing for pipeline exploration, not pretrained semantic embeddings.