# Student Performance Analysis

An exploratory data analysis of exam results for 1,000 students, aimed at finding which factors affect grades and which students are at risk of falling behind. The project covers data exploration, five factor-analysis questions, six visualisations, an at-risk student segmentation, and a Principal's Report with three actionable recommendations.

> Completed as part of the Pluto Academy Data Analytics Internship (Project 02).

---

## Problem Statement

As a data analyst hired by a school, analyse student performance data to:

- Understand which factors (parental education, test preparation, gender, family income) affect exam scores
- Identify students who are at risk of underperforming
- Give the principal three practical recommendations to improve outcomes in the next academic year

## Dataset

- **Source:** [Students Performance in Exams (Kaggle)](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
- **Size:** 1,000 student records and 8 columns

| Column | Meaning |
|---|---|
| `gender` | Male or female |
| `race` | Anonymised ethnic group (A to E) |
| `parent_edu` | Highest education level of the student's parents |
| `lunch` | Standard or free/reduced (used as a rough indicator of family income) |
| `test_prep` | Whether the student completed the test preparation course |
| `math`, `reading`, `writing` | Exam scores out of 100 |
| `total`, `average` | Columns created in this project (total out of 300, average out of 100) |

## Tools and Libraries

| Tool | Purpose |
|---|---|
| Python | Core analysis |
| Pandas, NumPy | Data exploration, grouping, calculations |
| Matplotlib, Seaborn | Visualisations |
| Google Colab | Development environment |
| GitHub | Version control and portfolio hosting |

## Approach

1. **Exploration and cleaning:** checked shape, data types, missing values and duplicates, renamed columns, and created `total` and `average` score columns.
2. **Factor analysis:** answered five questions using grouped averages, correlations and distributions.
3. **Visualisation:** built six charts, plus one extra chart for at-risk groups.
4. **At-risk segmentation:** defined an at-risk student as one scoring **below 50 in any subject**, then calculated the at-risk percentage for every group.
5. **Reporting:** wrote a Principal's Report inside the notebook.

## Questions Answered

1. Does parental education level affect scores?
2. Do students who complete test prep score higher?
3. What is the correlation between reading, writing, and math scores?
4. Which gender performs better in which subject?
5. What is the distribution of total scores?

## Visualisations

1. Box plot: total score by parental education
2. Bar chart: test prep completed vs not completed
3. Heatmap: correlation between math, reading and writing
4. Grouped bar chart: gender vs subject
5. Histogram: distribution of total scores
6. Scatter plot: reading vs math score
7. Bar chart: top 10 groups by at-risk percentage

All charts are visible in the notebook output.

## Key Findings

| Question | Result |
|---|---|
| Parental education | Master's degree: 220.80 average total score vs 189.29 for high school, a gap of 31.5 points |
| Test preparation | Completed: 218.01 vs none: 195.12, a difference of 22.9 points (11.7% higher) |
| Subject correlation | Reading and writing: 0.955. Math and reading: 0.82. Math and writing: 0.80 |
| Gender | Girls lead in reading (72.6 vs 65.5) and writing (72.5 vs 63.3). Boys lead in math (68.7 vs 63.6) |
| Score distribution | Average 203.3 out of 300, median 205, most common range 180 to 210 (26% of students) |

## At-Risk Student Segmentation

**Definition:** a student is at-risk if they score below 50 in any one subject.

- **188 of 1,000 students (18.8%)** are at-risk.
- Math has the most students below 50 (135), followed by writing (114) and reading (90).

| Group | Students | At-Risk | At-Risk % |
|---|---|---|---|
| Race: Group A | 89 | 30 | 33.7% |
| Lunch: free/reduced | 355 | 111 | 31.3% |
| Parental education: some high school | 179 | 46 | 25.7% |
| Parental education: high school | 196 | 49 | 25.0% |
| Test prep: none | 642 | 152 | 23.7% |

For comparison, students on standard lunch have an at-risk rate of 11.9%, and students who completed test prep have a rate of 10.1%. The full table is in the notebook.

## Recommendations

1. **Make test prep accessible to all students who need it**, starting with students on free/reduced lunch. Students without test prep make up 152 of the 188 at-risk students.
2. **Introduce subject-specific support, with a focus on math**, such as weekly small-group sessions, plus reading and writing workshops to narrow gender gaps.
3. **Set up an early-warning system and an after-school homework club** to flag students scoring below 50 after the first term and support those who may lack help at home.

The full Principal's Report is in the notebook under **"5. Principal's Report"**.

## Repository Structure

```
student-performance-analysis/
├── Student_Performance_Analysis.ipynb   # Full analysis notebook (exploration, charts, segmentation, report)
└── README.md                            # Project documentation
```

## How to Run

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams) and unzip it.
2. Open `Student_Performance_Analysis.ipynb` in [Google Colab](https://colab.research.google.com).
3. Upload the dataset zip file (or update the file path in the notebook).
4. Run all cells with **Runtime → Run all**.

## Limitations

- The dataset has only 1,000 students, and some groups are small (for example, Group A has 89 students), so percentages for those groups should be read with caution.
- The findings show **association, not causation**. For example, students who took test prep may also be more motivated.
- Factors overlap (a student can be in Group A, on free lunch, and without test prep), so the effect of each factor cannot be separated in this analysis.

## Author

**[Your Name]**
[LinkedIn](https://www.linkedin.com/in/your-profile) | [GitHub](https://github.com/your-username)
