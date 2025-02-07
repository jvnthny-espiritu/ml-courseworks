## **📂 Folder Structure**  
Each **activity** has its own folder. Inside each activity:  
- A `/dataset/` folder contains required data.  
- Each team member creates a **personal folder** inside the activity folder.  

```
/ml-courseworks
  ├── /k-means-activity
  │     ├── /dataset
  │     │     ├── penguins.csv  👈 (Dataset for the activity)
  │     ├── /your-name   👈 (Create your folder here!)
  │     │     ├── kmeans.ipynb
  │     │     ├── README.md
  │     ├── README.md  👈 (Activity instructions)
  ├── .gitignore
```

---

### **🔹 Step 1: Clone the Repository**  
If this is your first time working with the repo, **clone it** to your local machine:  
```sh
git clone https://github.com/jvnthny-espiritu/ml-courseworks.git
cd ml-courseworks
```

### **🔹 Step 2: Create a New Branch**  
Do not work directly on `main`. Instead, **create a new branch** with your name:  
```sh
git checkout -b k-means-your-name
```
🔹 **Replace `your-name`** with your **GitHub username or real name**.  

---

# **📊 Dataset Preparation & Feature Selection**  

### **🔹 Step 3: Load the Dataset**  
Inside your **Jupyter Notebook (`kmeans.ipynb`)**, load the dataset:  
```python
import pandas as pd

# Load dataset
df = pd.read_csv("../dataset/penguins.csv")  # Adjust path if needed

# Display first few rows
df.head()
```

### **🔹 Step 4: Clean the Dataset**  
Check for **missing values** and remove them:  
```python
# Check for missing values
print(df.isnull().sum())

# Drop missing values
df = df.dropna().reset_index(drop=True)
```

---

### **🔹 Step 5: Select Features for K-Means**  
For clustering, we will use **three numerical features**:  
1. **Culmen Length (`culmen_length_mm`)**  
2. **Culmen Depth (`culmen_depth_mm`)**  
3. **Flipper Length (`flipper_length_mm`)**  

Filter the dataset to these features:  
```python
selected_features = ["culmen_length_mm", "culmen_depth_mm", "flipper_length_mm"]
df_selected = df[selected_features]
```

---

### **🔹 Step 6: Select 100 Random Data Points**  
To reduce computation, sample **100 random rows** from the dataset:  
```python
df_sample = df_selected.sample(n=100, random_state=42).reset_index(drop=True)

# Display the sample dataset
df_sample.head()
```

---

# **🤖 K-Means Clustering Implementation**  
Now, apply K-Means clustering on the **df_sample** dataset.

### **🔹 Step 7: Apply K-Means Algorithm**  

---

# **📤 Submitting Your Work for Review**  

### **🔹 Step 8: Commit Your Changes**  
Once you've completed your notebook, **stage and commit** it:  
```sh
git add k-means-activity/your-name/
git commit -m "Added k-means clustering notebook"
```

### **🔹 Step 9: Push to GitHub**  
Send your branch to GitHub:  
```sh
git push origin k-means-your-name
```

---

## **📌 Step 10: Submit a Pull Request (PR) for Review by the Team Lead**  
1. **Go to the GitHub repository** in your browser.  
2. Click the **Pull Requests** tab → **New Pull Request**.  
3. Select:  
   - **Base branch:** `main`  
   - **Compare branch:** `k-means-your-name`  
4. **Describe your work** (e.g., what you did, any issues, findings).  
5. **Tag the Team Lead for review** in the PR comments.  
6. Click **Create Pull Request** and wait for feedback.  

---

# **📌 Step 11: Review & Merge**  
🔹 **Only the Team Lead will approve and merge PRs.**  
- If changes are needed, the lead will request them.  
- To make changes, update your files and **push again**:  
  ```sh
  git add .
  git commit -m "Updated notebook based on review"
  git push origin k-means-your-name
  ```
- Once approved, your PR will be **merged into `main`**. 🎉  

---

# **📌 Step 12: Sync Your Local Repo**  
After merging, **update your local repo** before starting a new activity:  
```sh
git checkout main
git pull origin main
```
Then, repeat the steps for the next activity! 🎯  

---

# **📌 Reminders**  
✅ **Follow the folder structure** – keep all files inside your personal folder.  
✅ **Use clear commit messages** (e.g., `"Completed k-means clustering"`).  
✅ **Request a PR review from the Team Lead before merging**.  
✅ **Check and respond to feedback on your PR**.  
✅ **Pull the latest changes** before working (`git pull origin main`).  
