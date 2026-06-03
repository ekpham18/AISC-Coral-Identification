# AISC-Coral-Identification

Our task: 
- Automate coral segmentation/identification using 3D photogrammetry model data. 

Core objectives: 
- Distinguish coral tissue from substrate (plugs, settlement structures)
- Distinguish coral from algae growth
- Crop/isolate individual coral colonies automatically
- Export isolated coral 3D models for morphological analysis

Challenges:
- Identify coral vs. algae with similar colors
- Working in 3D space
  
End goal:
- Replace manual segmentation normally achieved with Autodesk Recap Photo
- Enable automated extraction of metrics (volume, height, width, surface complexity, substrate coverage)

---

## Running the seaboard visualization locally

### 1. Install Google Drive for Desktop
Download and install from https://www.google.com/drive/download/

- Sign in with your Google account
- In preferences, make sure sync mode is set to **Stream files** (not Mirror) — this means files are only downloaded when you open them, not all at once

### 2. Install dependencies
```bash
pip install open3d plotly numpy
```

### 3. Open the notebook
Open `src/toby_seaboard_data.ipynb` in VS Code (requires the Jupyter extension).

### 4. Set your Google account
In **Cell 0**, update the email to match your Google account:
```python
GOOGLE_ACCOUNT = "your-email@gmail.com"
```

### 5. Run the notebook
- Run **Cell 0** — should print `Path exists: True`
- Run **Cell 1** — loads libraries and defines the plot function
- Run any seaboard cell to render an interactive 3D mesh

> Note: Seaboard 6 is missing from the Drive folder and will show "File not found" — this is expected.
