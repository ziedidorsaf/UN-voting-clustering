# UN General Assembly Voting Patterns: Clustering Analysis

A comprehensive data science project analyzing UN General Assembly voting patterns from 1946-2019 using machine learning clustering techniques to identify voting blocs among 200 countries.

##  Project Overview

This project applies unsupervised machine learning techniques to analyze historical UN voting data and identify patterns in how countries vote on international resolutions. By clustering countries based on their voting behavior, we can discover geopolitical voting blocs and understand international relations dynamics.

### Key Objectives
- Apply K-means clustering to real-world diplomatic data
- Implement hierarchical clustering for comparison
- Validate clustering results using appropriate metrics
- Visualize and interpret clustering results in a geopolitical context
- Compare different clustering methodologies

##  Dataset

The analysis uses three main datasets covering UN General Assembly voting patterns:

- **869,937 individual votes** from 200 countries
- **6,202 resolutions** across various topics and time periods
- **Time span:** 1946-2019 (73 years of UN voting history)

### Data Files
- `unvotes.csv` - Individual country votes on UN resolutions
- `roll_calls.csv` - Information about each UN resolution
- `issues.csv` - Categories and topics of resolutions

### Vote Types
- **Yes** (1): Support for the resolution
- **No** (-1): Opposition to the resolution  
- **Abstain** (0): Neutral stance or non-participation

## 🛠 Technical Implementation

### Technologies Used
- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Scikit-learn** - Machine learning algorithms and metrics
- **Matplotlib & Seaborn** - Data visualization
- **SciPy** - Statistical analysis and hierarchical clustering

### Machine Learning Techniques

#### 1. Data Preprocessing
- Vote encoding (Yes=1, Abstain=0, No=-1)
- Country-resolution voting matrix creation
- Data quality filtering (minimum 50% participation)
- Missing value imputation
- Feature standardization using StandardScaler
- Constant feature removal

#### 2. K-means Clustering
- Optimal cluster determination using:
  - Elbow method (inertia analysis)
  - Silhouette score optimization
- Cluster validation and interpretation
- Country assignment to voting blocs

#### 3. Hierarchical Clustering
- Agglomerative clustering with Ward linkage
- Dendrogram visualization
- Comparison with K-means results

#### 4. Model Evaluation
- **Silhouette Score** - Cluster quality assessment
- **Adjusted Rand Index** - Agreement between clustering methods
- **Principal Component Analysis (PCA)** - Dimensionality reduction for visualization

##  Key Features

### Analysis Components
1. **Exploratory Data Analysis** - Understanding vote distributions and patterns
2. **Data Preprocessing Pipeline** - Clean, transform, and prepare data for clustering
3. **Optimal Cluster Selection** - Systematic approach to determine best number of clusters
4. **Comparative Analysis** - K-means vs. Hierarchical clustering evaluation
5. **Geopolitical Visualization** - PCA-based plotting with country highlighting
6. **Results Interpretation** - Real-world context for discovered voting blocs

### Visualizations
- Elbow plots for optimal K selection
- Silhouette score analysis
- Hierarchical clustering dendrograms
- PCA scatter plots with cluster coloring
- Key country highlighting (US, Russia, China, UK, France, etc.)

##  Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
```

### Installation
1. Clone the repository:
```bash
git clone https://github.com/ziedidorsaf/un-voting-clustering.git
cd un-voting-clustering
```

2. Download the dataset files and ensure they're in the project directory:
   - `unvotes.csv`
   - `roll_calls.csv` 
   - `issues.csv`

3. Launch Jupyter Notebook:
```bash
jupyter notebook UN_Voting_Clustering_Student_Lab.ipynb
```

### Running the Analysis
Execute the cells in sequence:
1. **Setup and Data Loading** - Import libraries and load datasets
2. **Data Preprocessing** - Clean and transform the voting data
3. **K-means Clustering** - Find optimal clusters and apply K-means
4. **Hierarchical Clustering** - Apply agglomerative clustering
5. **Model Comparison** - Evaluate and compare both methods
6. **Visualization** - Generate PCA plots and interpretations

##  Project Structure

```
un-voting-clustering/
│
├── UN_Voting_Clustering.ipynb                # Main analysis notebook
├── unvotes.csv                               # Individual country votes
├── roll_calls.csv                            # Resolution information
├── issues.csv                                # Resolution categories
├── README.md                                 # Project documentation
```


##  Educational Value

This project demonstrates:
- **Real-world application** of unsupervised learning
- **Data preprocessing** techniques for messy, real-world data
- **Model validation** and comparison methodologies
- **Dimensionality reduction** for high-dimensional data visualization
- **Domain expertise integration** - combining ML with geopolitical knowledge

##  Performance Metrics

The project evaluates clustering quality using:
- **Silhouette Score**: Measures cluster cohesion and separation
- **Inertia/Within-cluster Sum of Squares**: K-means optimization metric
- **Adjusted Rand Index**: Agreement between different clustering methods
- **Explained Variance Ratio**: PCA dimensionality reduction effectiveness


## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
