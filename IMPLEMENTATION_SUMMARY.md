# Implementation Summary

## Assignment: Modularity on the Karate Club Graph (DSC212)

### Deliverable
✅ **Jupyter notebook (`karate_club_modularity.ipynb`)** that runs top-to-bottom without manual edits

### Repository
- URL: https://github.com/CodeCurator-OP/Assignment-DSC-211-Modularity

## Implementation Details

### 1. Core Algorithm Components

#### Modularity Matrix Computation
- Implemented: `B = A - (k * k^T) / (2m)`
- Properly handles subgraphs for recursive bisection
- Maintains reference to original graph's edge count (m)

#### Spectral Bipartition
- Eigenvalue decomposition using scipy.linalg.eigh (optimized for symmetric matrices)
- Extracts leading eigenvector u₁ corresponding to largest eigenvalue λ₁
- Splits nodes by sign of eigenvector entries
- Implements stopping criterion: λ₁ ≤ 0

#### Recursive Bisection
- Iteratively applies spectral bipartition
- Tests each community independently
- Stops when no community can be split beneficially
- Tracks all iterations with complete state information

### 2. Visualizations

#### Graph Visualization
- Fixed spring layout (seed=42) for consistency across iterations
- Color-coded communities with distinct colors
- Node labels showing IDs
- Legend indicating community sizes
- Generated at each iteration

#### Metric Evolution Plots
For each of the 4 metrics:
- Line plot for selected key nodes (leaders, top/bottom centrality)
- Heatmap showing all nodes across all iterations
- Clear axis labels and titles

### 3. Centrality Metrics

All computed using NetworkX built-in functions:
1. **Degree Centrality**: `nx.degree_centrality(G)`
2. **Betweenness Centrality**: `nx.betweenness_centrality(G)`
3. **Closeness Centrality**: `nx.closeness_centrality(G)`
4. **Clustering Coefficient**: `nx.clustering(G)`

Tracked at every iteration to show evolution.

### 4. Analysis and Discussion

Comprehensive discussion section covering:
- Community detection results and ground truth comparison
- How each centrality metric behaves across splits
- Why certain nodes remain central vs. lose centrality
- Role of bridge nodes and community leaders
- Mathematical insights into the modularity approach
- Stability of local vs. global metrics

### 5. Documentation

- Abstract explaining the assignment
- Attribution to Newman (2006) PNAS paper
- Mathematical notation consistent with problem statement
- Clear function docstrings
- Step-by-step explanations in markdown cells
- Complete references section

## Results

### Community Detection
- **Final communities**: 2 groups (18 and 16 nodes)
- **Ground truth validation**: ✅ Mr. Hi (node 0) and President (node 33) correctly separated
- **Iterations**: 1 split (optimal for this dataset)
- **Leading eigenvalue**: λ₁ = 17.107387

### Top Central Nodes
**Degree Centrality:**
1. Node 33 (President): 0.5152
2. Node 0 (Mr. Hi): 0.4848
3. Node 32: 0.3636

**Betweenness Centrality:**
1. Node 0 (Mr. Hi): 0.4376
2. Node 33 (President): 0.3041
3. Node 32: 0.1452

Both faction leaders identified as the two most central nodes.

## Testing

### Validation Performed
✅ Notebook executes completely from top to bottom
✅ All visualizations generated successfully
✅ Modularity matrix is symmetric
✅ Eigenvalue stopping criterion works correctly
✅ Communities match historical split
✅ All four centrality metrics computed correctly
✅ Evolution plots display properly

### Test Command
```bash
jupyter nbconvert --to notebook --execute karate_club_modularity.ipynb
```

## Dependencies

- Python 3.8+
- numpy
- networkx
- matplotlib
- scipy
- jupyter

All available via: `pip install numpy networkx matplotlib scipy jupyter`

## Academic Integrity

This is an original implementation based on the mathematical specification provided in the assignment. The modularity method and its mathematical foundation are properly attributed to Newman (2006).

## Submission Checklist

- [x] Jupyter notebook (.ipynb) created
- [x] Runs top-to-bottom without manual edits
- [x] Contains all required code
- [x] Contains all required visualizations
- [x] Contains all required metrics
- [x] Contains discussion and analysis
- [x] Properly cited (Newman 2006)
- [x] Uploaded to GitHub repository
- [x] README with usage instructions
- [x] Tested and validated

**Status: COMPLETE AND READY FOR SUBMISSION** ✅
