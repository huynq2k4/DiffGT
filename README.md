# Diffusion Graph Transformer
This is my implementation of the paper "A Directional Diffusion Graph Transformer for Recommendation" (Zixuan Yi, Xi Wang, Iadh Ounis).
## Dataset
I run on two out of three datasets mentioned in the paper: MovieLens-1M and FourSquare. All the datasets have been preprocessed to align with the input of the implementation.
## Experiments
The results on two datasets are unstable. Highest value for each dataset:
- FourSquare: 0.3292 (Recall@20), 0.6089 (NDCG@20)
- MovieLens-1M: 0.2430 (Recall@20), 0.2871 (NDCG@20)

Average time to run each component:
- Graph encoder (LightGCN): 0.22s (FourSquare), 0.235s (MovieLens-1M)
- Diffusion model with linear transformer: 0.011s (FourSquare), 0.016s (MovieLens-1M)
- Embedding extraction after diffusion: 0.004s (FourSquare), 0.0078s (MovieLens-1M)
- Loss: 0.021s (FourSquare), 0.028s (MovieLens-1M)
