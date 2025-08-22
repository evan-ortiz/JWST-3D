![](docs/assets/banner1.png)
## 📌 Abstract 

The **James Webb Space Telescope (JWST)**, with its advanced infrared capabilities, enables humanity to peer back **13.5 billion years** into the early universe. Equipped with instruments such as the **Near-Infrared Camera (NIRCam)** for detecting star formation and galaxy evolution, and the **Mid-Infrared Instrument (MIRI)** for analyzing cooler objects like planetary atmospheres and distant galaxies, JWST has opened new windows into cosmic exploration.  

All JWST data are stored and made publicly available through the **Mikulski Archive for Space Telescopes (MAST)**. This open-source approach allows researchers worldwide to engage with cutting-edge astrophysical datasets.  

In this project, we focused on **protoplanetary disk IRAS-04385**, located **456 light-years away**, using over **200 GB of publicly available JWST data** from the MAST archive. Protoplanetary disks are dense, gas-and-dust-filled regions surrounding young stars, where planetary systems form and water, essential for life, can often be found. 

Our analysis revealed that IRAS-04385 is a **promising candidate in the search for habitable worlds**, contributing to the growing catalog of over **5,500 known exoplanets**. Compared to the **2009 baseline study**, our results demonstrate a **clearer image and a broader infrared spectrum**, highlighting the progress enabled by JWST.  

---
## 🔮 Future Directions  

Beyond reproducing scientific findings, this project lays the foundation for **future innovations and data exploration**:  
### 3D Galaxy Mapping  
- Building **3D models of the universe** using **infrared intensity and distance as axes**, creating interactive galactic maps.  
- Incorporating **graphs comparing distances from Earth** across observed stellar systems using red shift.  
- Using **predictive modeling with path exclusion** to interpolate unexplored regions of space.  
- Integrating links to open datasets from [data.nasa.gov](https://data.nasa.gov) and outreach material such as [JWST Webinars](https://www.stsci.edu/jwst/science-execution/jwebbinars).  
- Embedding **QR codes** to allow interactive exploration within visualizations.  

### DataCube Applications for JWST  
- Developing **DataCube analysis pipelines** for large JWST datasets.  
- Exploring connections to projects like **Q3Dfit** (spectral cube fitting) for galaxy analysis.  
- Using **lmfit (Python)** for non-linear spectral fitting.  
- Applying **ppxf (Penalized Pixel-Fitting)** for stellar population and kinematic modeling.  

### Automation and Computer Vision  
- Creating **computer vision pipelines** to automatically sift through JWST data at scale.  
- Targeting discovery of **the oldest galaxies and stellar structures** in the universe. 
---
# JWST Data Project Documentation

## 1. Important Links

- [JWST Webinars](https://www.stsci.edu/jwst/science-execution/jwebbinars)  
- [Andrea Banzatti Lecture (YouTube)](https://www.youtube.com/watch?v=KGK5qwrg0wI&t=359s)  
- [MAST Homepage](https://archive.stsci.edu/missions-and-data/jwst)  
- [JWST GitHub](https://github.com/spacetelescope/jwst)  
- [NASA Official Proposal (PDF)](https://www.stsci.edu/jwst/phase2-public/1640.pdf)  
- [STScI Environment (stenv)](https://github.com/spacetelescope/stenv/releases#)  
- [JWST Webinars YouTube Channel](https://www.youtube.com/@JWSTObserver)  
- [MAST Data Repository](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html)  
- [Specific Data Link (IRAS-04385)](https://mast.stsci.edu/search/ui/#/jwst/results?resolve=true&data_types=image,measurements,spectrum,timeseries,other&instruments=MIRI,FGS,NIRCAM,NIRSPEC,NIRISS&pi_surname=Banzatti&custom_col_sel_1=targprop&custom_col_val_1=IRAS-04385&useStore=false&search_key=3e8e5bcb8a256)  
- [NASA Open Source Code](https://code.nasa.gov/)  
- [NASA Open Data Sets](https://data.nasa.gov/)  

---
## 2. Datathon Challenges

## 📅 Datathon Details  

This project was completed as part of a **week-long data science coding marathon and contest** during **Love Data Week (February 12–16, 2024)**.  

- **Maximum team size:** 4 members  
- **Kickoff Event:** Monday, Feb. 12 (open talk and team formation)  
- **Independent Work:** Teams worked on their projects throughout the week  
- **Final Presentation:** Friday, Feb. 16 (1:00–3:00 pm, in-person)  

### Participation Guidelines  
- All work on the project must be completed during Love Data Week (Feb. 12–16).  
- Teams may seek advice from organizers, librarians, and specialists.  
- Projects must be chosen from the approved topic pool.  
- **Open data sources must be cited appropriately.**  
- Libraries and open-source code may be used in project development.  
- Teams using AI tools must disclose usage and provide a verification statement regarding accuracy.  
- Deliverables include a **digital poster** and uploaded **final dataset** to TXST online repositories (deadline: 1:00 pm, Feb. 16).  
- Teams must present their project in a **5–10 minute oral presentation** alongside their digital poster.  

### Tools and Resources Provided  
- Open data resources  
- Example research questions & datasets  
- Research Data Management (RDM) best practices  
- Instructions for depositing the final project into repositories  
- Data citation guidelines  
- Open access books on **R for data analysis and visualization**  

---
## 3. Accessing JWST Data  

JWST data is hosted on the [MAST Portal](https://outerspace.stsci.edu/display/MASTDOCS/Portal+Guide).  

- No account is required for browser downloads (tested in Chrome).  
- Raw image files can be **~12 GB each**, so bulk downloads are slow.  
- API access is available with documentation: [MAST API Guide](https://mast.stsci.edu/api/v0/index.html).  
- JWST-specific documentation: [Accessing JWST Data](https://jwst-docs.stsci.edu/accessing-jwst-data).  

### Dataset Selection  
We used data from [Dr. Andrea Banzatti](https://news.txst.edu/research-and-innovation/2022/texas-state-physicist-to-study-water-delivery-to-exoplanets.html) (Texas State University, Physics Department). His research focuses on **gas and dust evolution in protoplanetary disks**.  

- Target: **IRAS-04385**  
- Project Overview: [NASA Proposal 1640](https://www.stsci.edu/jwst/phase2-public/1640.pdf)  
- Dataset link: [MAST Portal Filtered Data](https://mast.stsci.edu/search/ui/#/jwst/results?resolve=true&data_types=image,measurements,spectrum,timeseries,other&instruments=MIRI,FGS,NIRCAM,NIRSPEC,NIRISS&pi_surname=Banzatti&custom_col_sel_1=targprop&custom_col_val_1=IRAS-04385&useStore=false&search_key=3e8e5bcb8a256)  

**Filter Criteria (manual selection):**  
- PI Surname = Banzatti  
- Alternative Target Name = IRAS-04385  

---

## 4. Project Files  

| ArchiveFileID | fileSetName               | productLevel   | targprop   | exp_type | program | pi_name          | opticalElements               |
| ------------- | ------------------------- | -------------- | ---------- | -------- | ------- | ---------------- | ----------------------------- |
| 81300700      | jw01640011001_02101_00001 | 1b, 2a, 2b     | IRAS-04385 | MIR_TACQ | 1640    | Banzatti, Andrea | FND                           |
| 81301248      | jw01640011001_04101_00001 | 1b, 2a, 2b, 2c | IRAS-04385 | MIR_MRS  | 1640    | Banzatti, Andrea | CH12;SHORT, CH34;SHORT, F770W |
| …             | …                         | …              | …          | …        | …       | …                | …                             |

*(Full dataset table retained, truncated here for readability.)*

---

## 5. System Environment  

- **OS:** Ubuntu Linux  
- **CPU:** Intel(R) Core(TM) i7-14700K  
- **GPU:** NVIDIA RTX 4080 Super  
- **RAM:** 64 GB  

---

## 6. Setup Instructions  

1. Install [Miniconda](https://docs.anaconda.com/free/miniconda/index.html).  
2. Download the [STScI environment (stenv)](https://github.com/spacetelescope/stenv/releases).  

### Conda Environment Setup  

```bash
conda env create --name stenv --file "https://github.com/spacetelescope/stenv/releases/download/2024.02.05/stenv-Linux-X64-py3.10-2024.02.05.yaml"

conda activate stenv
pip install git+https://github.com/spacetelescope/jdaviz --upgrade
conda install bottleneck
conda install -c conda-forge notebook jupyterlab voila
```

- [Jdaviz Installation Guide](https://jdaviz.readthedocs.io/en/latest/installation.html)  

---

## 7. Working with the Data  

### MIRI MRS Data  

- Found in the **OBS MODE = MIR_MRS** column.  
- Data is split into **3 band lengths** (SHORT, MEDIUM, LONG), with **2 channels each (12, 34)**.  
- Analysis requires processing all 6 combinations.  

**File naming notes:**  
- \`*_uncal.fits\`: Uncalibrated input data.  
- Background calibration files are downloaded into the \`crds_cache\` folder automatically.  

---

## 8. Processing Pipeline  

We used NASA’s [MRS_FlightNB1 Notebook](https://github.com/STScI-MIRI/MRS-ExampleNB/blob/main/Flight_Notebook1/MRS_FlightNB1.ipynb).  

**Steps:**  
1. Place all \`uncal\` files in a \`sci_input\` folder.  
2. Run the notebook **six times**, once per band/channel pair:  
   - 12, SHORT  
   - 12, MEDIUM  
   - 12, LONG  
   - 34, SHORT  
   - 34, MEDIUM  
   - 34, LONG  

```python
use_ch = ''    # '12' or '34'
use_band = ''  # 'SHORT', 'MEDIUM', 'LONG'
```

- Runtime: ~2 hours on listed system.  
- Output: \`spectra.png\` (master wavelength table) + multiple data cubes.  

### Cube Visualization  

```bash
jdaviz --layout=cubeviz /path/to/cube.fits
```

---

## 9. Results  

### Reference Data: IRAS-04385 (Schaefer et al. 2009)  
![](docs/assets/Pasted%20image%2020240215190050%201.png)  

### Processed Output (Initial Analysis)  
![](docs/assets/spectra%201.png)  
![](docs/assets/bqplot%20(1)%201.png)  
![](docs/assets/bqplot%20(3)%201.png)  

---

## 10. Final Deliverable  

![](docs/assets/Dataposter.pdf)
