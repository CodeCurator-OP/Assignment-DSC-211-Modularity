# Assignment-DSC-211-Modularity

## Spectral Modularity Analysis on the Karate Club Graph

This repository contains a Jupyter notebook implementing spectral modularity-based community detection on Zachary's Karate Club network for the DSC212 Graph Theory module.

## Contents

- `karate_club_modularity.ipynb` - Complete implementation with code, visualizations, and analysis

## What's Implemented

The notebook implements a complete spectral modularity analysis including:

1. **Modularity Matrix Computation**: Implementation of B = A - kk^T/2m
2. **Spectral Bipartition**: Using the leading eigenvector for community splitting
3. **Recursive Bisection**: Multi-community detection with eigenvalue stopping criterion (λ₁ ≤ 0)
4. **Visualizations**: 
   - Graph visualization at each iteration with color-coded communities
   - Evolution plots for all centrality metrics
   - Heatmaps showing metric changes across iterations
5. **Centrality Metrics**: Computation of degree, betweenness, closeness, and clustering coefficients
6. **Analysis**: Comprehensive discussion of results and findings

## Requirements

The notebook requires the following Python packages:
- numpy
- networkx
- matplotlib
- scipy
- jupyter

Install dependencies with:
```bash
pip install numpy networkx matplotlib scipy jupyter
```

## Running the Notebook

1. Clone the repository
2. Install dependencies
3. Open the notebook:
   ```bash
   jupyter notebook karate_club_modularity.ipynb
   ```
4. Run all cells from top to bottom

The notebook is designed to run completely from top to bottom without any manual edits.

## Results

The implementation successfully:
- Detects 2 primary communities matching the real-world split
- Places Mr. Hi (node 0) and the President (node 33) in separate communities
- Tracks how centrality metrics evolve as community structure is discovered
- Provides insights into which nodes remain central across splits

## Attribution

The modularity method is based on:

**Newman, M. E. J. (2006). "Modularity and community structure in networks." PNAS 103(23):8577–8582.**

## Author

Implementation for DSC212: Graph Theory Module