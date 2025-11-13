# How to View All Visualizations

This repository now contains all executed code with complete visualizations!

## Quick Start: View Results Immediately

### Option 1: View HTML File (Recommended - No Setup Required)
1. Download or open `karate_club_modularity.html` 
2. Open it in any web browser (Chrome, Firefox, Safari, Edge, etc.)
3. All visualizations and results are embedded and ready to view!

### Option 2: View on GitHub
1. Navigate to `karate_club_modularity.ipynb` on GitHub
2. GitHub will render the notebook with all visualizations inline
3. All plots, graphs, and analysis are visible directly in the browser

### Option 3: Open in Jupyter Notebook
If you have Jupyter installed:
```bash
jupyter notebook karate_club_modularity.ipynb
```

## What Visualizations Are Included?

All visualizations have been pre-generated and embedded:

### 1. Network Visualizations (3 plots)
- **Initial Graph**: The complete Karate Club network (34 nodes, 78 edges)
- **Iteration 0**: All nodes in single community
- **Iteration 1**: Network split into 2 communities (color-coded)

### 2. Centrality Metric Evolution (4 sets of plots = 8 total plots)
Each metric has TWO visualizations:
- **Line Plot**: Shows evolution of key nodes (including Mr. Hi and the President)
- **Heatmap**: Shows all 34 nodes across all iterations

Metrics tracked:
1. **Degree Centrality**: Direct connections
2. **Betweenness Centrality**: Bridge positions
3. **Closeness Centrality**: Proximity to all others  
4. **Clustering Coefficient**: Local cohesion

### 3. Summary Statistics
- Final community structure (which nodes are in which community)
- Top 5 nodes ranked by each centrality metric
- Identification of faction leaders (Mr. Hi vs President)

## Total Visualizations: 7 Images
- 3 network graphs
- 4 metric evolution plots (each with line plot + heatmap in single figure)

## File Sizes
- `karate_club_modularity.ipynb`: 857 KB (with embedded images)
- `karate_club_modularity.html`: 1.2 MB (standalone HTML)

## Notes
- All outputs are already generated - no need to run the code
- The notebook can still be re-executed if you want to modify parameters
- All visualizations use consistent node positioning for easy comparison
- Color-coding makes community structure immediately visible
