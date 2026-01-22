# Semantic Cache Experiment

Testing Redis's claim that fine-tuned embedding models outperform general-purpose models for semantic caching.

## Background

- **Paper**: [Advancing Semantic Caching for LLMs with Domain-Specific Embeddings and Synthetic Data](https://arxiv.org/abs/2504.02268)
- **Models**: [redis/langcache-embed-v3-small](https://huggingface.co/redis/langcache-embed-v3-small)
- **Substack Post**: [When Your Cache Thinks "Pet-Friendly" Means "No Pets Allowed"](https://joesack.substack.com/)

## Key Finding

At threshold 0.7, the cache-optimized model achieves 0.75 F1 vs 0.33 for the general-purpose baseline on real estate query pairs.

The dangerous case: "pet-friendly apartment" vs "no pets allowed policy" scores 0.57 with the baseline (potential false cache hit) but only 0.34 with LangCache (correctly rejected).

## Files

- `semantic_cache_experiment.ipynb` - Main notebook
- `test_pairs.json` - Real estate query pairs with ground truth labels

## Requirements

```bash
pip install sentence-transformers numpy matplotlib
```

## License

MIT
