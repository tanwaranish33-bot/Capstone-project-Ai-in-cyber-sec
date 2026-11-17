# Mini AI Cybersecurity Assistant – Capstone

**Course:** ENSP355 – AI in Cyber Security  
**Platform:** Jupyter Notebook / Google Colab

## Files
- `Mini_AI_Cybersecurity_Assistant.ipynb` – integrated capstone notebook.
- `messages.csv` – synthetic message samples.
- `login_activity.csv` – synthetic login activity records.
- `Capstone_Report.md` – 2–3 page style report.
- `Responsible_Use_Checklist.md` – one-page safety and review checklist.
- `Individual_Contribution_Statement_Template.md` – complete if required for team work.
- `requirements.txt` – Python dependencies.

## Run in Jupyter
1. Extract this ZIP.
2. Open a terminal in the extracted folder.
3. Install packages: `pip install -r requirements.txt`
4. Run `jupyter notebook` or `jupyter lab`.
5. Open `Mini_AI_Cybersecurity_Assistant.ipynb`.
6. Select **Kernel → Restart & Run All**.

Keep the notebook and both CSV files in the same folder.

## Run in Google Colab
1. Upload the notebook and CSV files to the same Google Drive folder, or upload the ZIP and extract it.
2. Open the notebook in Google Colab.
3. Ensure the two CSV files are available in the Colab working directory (upload them in the Files panel if needed).
4. Select **Runtime → Run all**.
5. Download the executed notebook and `final_combined_results.csv`.

## GitHub upload
Create a repository, extract this ZIP, and upload the project files. Or run:
```bash
git init
git add .
git commit -m "Add AI cybersecurity capstone assistant"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```
Replace the remote URL with your own repository URL.

## Important data note
The assignment PDF describes supplied synthetic/sanitized data, but separate CSV source files were not attached. The two CSVs in this project are newly created synthetic teaching examples. Do not present them as university-provided datasets. If your instructor supplied official Lab datasets separately, substitute them after checking the column names and labels.

## Scope and safety
This is an educational prototype, not a production security product. Do not use real personal data, test live accounts or networks, open suspicious links, or execute malware. Model predictions are not proof; high-risk, conflicting or low-confidence results require authorized human review.

## Documentation
- Python: https://docs.python.org/3/
- pandas: https://pandas.pydata.org/docs/
- scikit-learn: https://scikit-learn.org/stable/
- Matplotlib: https://matplotlib.org/stable/
- Jupyter: https://jupyter.org/documentation
- Google Colab: https://colab.research.google.com/
