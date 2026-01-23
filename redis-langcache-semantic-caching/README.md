# Redis LangCache Semantic Caching Experiment

Testing Redis's LangCache embedding models vs general-purpose MiniLM for semantic cache hit detection.

## Key Finding

At threshold 0.7, the cache-optimized model achieves 0.75 F1 vs 0.33 for the general-purpose baseline on real estate query pairs.

## Files

- `semantic_cache_experiment.ipynb` - Interactive notebook to run the experiments
- `test_pairs.json` - Real estate query pairs used for testing

## Quick Start

```bash
pip install sentence-transformers numpy matplotlib
jupyter notebook semantic_cache_experiment.ipynb
```

## Related

- Blog post: [Same Question, Different Words](https://joesack.substack.com/p/same-question-different-words)
- Model: [redis/langcache-embed-v3-small](https://huggingface.co/redis/langcache-embed-v3-small)
