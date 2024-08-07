# NLP Resume Extraction - Project Document

## Team Member Details
- **Group Name:** Lone Data Enthusiast
- **Team Members:**
  1. Name: Ritu Kukreja<br>
     Email: rk977@drexel.edu<br>
     Country: United States<br>
     College/Company: Drexel University<br>
     Specialization: Data Science, NLP, Data Analyst<br>

# Problem Description
The objective of this analysis is to explore and understand the dataset containing resume information. The dataset includes details such as name, designation, companies worked at, skills, graduation year, college name, degree, location, and years of experience.

# Exploratory Data Analysis (EDA)

### Task 1: Understanding the Landscape

I kick off our journey with a glance at the overall landscape. Using Python and data visualization libraries, I obtain a summary of the dataset and delve into statistical measures, offering a bird's-eye view of the resumes.

```python
print(resume_df.info())
print(resume_df.describe())
```

### Task 2: Peering into Graduation Years

The graduation year is a pivotal milestone in one's career journey. By creating a histogram, we visualize the distribution of graduation years, gaining insights into the academic timelines of professionals.

```python
plt.figure(figsize=(12, 6))
plt.subplot(1, 2, 1)
resume_df['Graduation Year'].hist(bins=20, edgecolor='k')
plt.title('Distribution of Graduation Year')
plt.show()
```

### Task 3: Decoding Categorical Features

Categorical features such as designation, companies, skills, college names, degree, and location add richness to the narrative. We unravel the uniqueness of each category by exploring the frequency of values.

```python
for col in ['Designation', 'Companies', 'Skills', 'College Name', 'Degree', 'Location']:
    print(f"Unique values in {col}:")
    print(resume_df[col].value_counts())
    print("\n")
```

### Task 4: The Language of Skills

Skills are the building blocks of a professional's identity. I employ a word cloud to visually represent the prominence of skills, creating a captivating display of the diverse skill sets present in the resumes.

```python
skills_text = ' '.join(resume_df['Skills'].astype(str))
wordcloud = WordCloud(width=800, height=400, background_color='white').generate(skills_text)
plt.figure(figsize=(10, 5))
plt.imshow(wordcloud, interpolation='bilinear')
plt.axis('off')
plt.title('Skills Word Cloud')
plt.show()
```

### Task 5: Mapping Careers geographically

The geographical distribution of professionals provides insights into hubs of professional activities. A countplot allows us to visualize the distribution of professionals across different locations.

```python
plt.figure(figsize=(20, 14))
sns.countplot(x='Location', data=resume_df, order=resume_df['Location'].value_counts().index)
plt.title('Distribution of Professionals by Location')
plt.xticks(rotation=90, ha='right')
plt.show()
```

## Insights Unveiled

My journey through this resume dataset has unraveled a plethora of insights. From academic timelines to skills shaping professional identities, each visual tells a story. Geographical distributions, career durations, and notable companies provide a holistic view of the professional landscape.

## Embracing Data for Career Exploration

As I conclude EDA, I recognize the power of data in unraveling the narratives embedded in resumes. Whether you're a career enthusiast or a data enthusiast, this journey through resumes showcases the fusion of technology and human experiences.

Lone Data Enthusiast<br>
10/26/2023
