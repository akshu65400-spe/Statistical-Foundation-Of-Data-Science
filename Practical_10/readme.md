🍷 Wine Dataset Analysis – Alternate Version

This project performs a complete analysis of the Wine Dataset using Python, including statistics, visualization, feature scaling, and PCA.
This version is different from the original solution by using different features, plots, and styles.

✅ Tasks Performed
1. Basic Statistics

Displayed summary statistics using:

describe()

2. Boxplot by Class Labels

Plotted malic_acid distribution for each wine class.

3. Scatterplot (Two Variables)

Used:

flavanoids

proanthocyanins
with class-based coloring.

4. Covariance Matrix

Generated a heatmap using a magma color palette.

5. Data Scaling

Scaled all numerical features using:

StandardScaler()

6. PCA for Class Separation

Reduced dimensionality to 2 components and visualized clustering.

📂 Project Structure
Wine-Analysis-Alt/
│
├── wine_alt_analysis.py
└── README.md

🔧 Installation
git clone https://github.com/<your-username>/Wine-Analysis-Alt.git
cd Wine-Analysis-Alt
pip install numpy pandas matplotlib seaborn scikit-learn

▶️ Running the Script
python wine_alt_analysis.py

📊 Output Visuals

The script generates:

Summary statistics

Boxplot of malic acid by class

Scatterplot of flavanoids vs proanthocyanins

Covariance matrix heatmap

Scaled feature dataset

PCA-based class separation plot

🧪 Libraries Used

pandas

numpy

matplotlib

seaborn

scikit-learn
