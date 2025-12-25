# TOPCAT H-R Diagram & Isochrone Workflow

This document summarizes the step-by-step procedure used to create H-R diagrams and fit isochrones for the Hyades and 47 Tucanae clusters.

---

## 1. Data Preparation
- Select the target cluster (Hyades or 47 Tucanae).  
- Extract the relevant Gaia EDR3 data. Focus on key parameters: 
  - Right Ascension (RA) [degrees]
  - Declination (Dec) [degrees]
  - Parallax [mas]
  - Photometric magnitudes (G, BP, RP)  

> Note: The actual Gaia data files are not included due to size.

---

## 2. Import into TOPCAT
- Open TOPCAT.  
- Load the Gaia data for the cluster.  
- Add new columns for:
  - Absolute magnitude (G_abs)  
  - Distance in parsecs (from parallax, `d = 1000 / parallax`)  

---

## 3. Clean Astrometric Errors
- Identify stars with high astrometric excess noise.  
- Exclude these stars to reduce noise in the H-R diagram.

---

## 4. Clean Photometric Errors
- Plot BP-RP color vs. phot_bp_rp_excess_factor.  
- Define a region to exclude stars with unreliable photometry.

---

## 5. H-R Diagram Creation
- Plot color (BP-RP) vs. absolute magnitude (G_abs).  
- Observe the main sequence, giant branch, and white dwarf branch.  
- Confirm that outliers are removed after previous cleaning steps.

---

## 6. Isochrone Fitting
- Download isochrones in the Gaia EDR3 photometric system (range of ages and metallicities).  
- Import isochrones into TOPCAT.  
- Overlay isochrones on the H-R diagram:
  - Third variable = Age (determine best-fitting isochrone for age).  
  - Similarly, evaluate metallicity.  

---

## 7. Final Diagrams
- Save final cleaned H-R diagrams.  
- Save isochrone-overplotted diagrams.  
- These diagrams illustrate cluster age and metallicity estimation.
