# Predictive-model-of-lens-touch
This repository provides a two-dimensional geometric eye model designed to identify eyes at high anatomical risk for iatrogenic lens touch during pars plana vitrectomy (PPV).

## 1. Overview
This contains an interactive eye model simulator. It allows users to input ocular biometric parameters and visualize whether the surgical trajectory (from trocar to posterior eye segments) intersects with the crystalline lens. The tool provides a graphical illustration comparable to R-based plots described in the manuscript.  

The model is intended to **illustrate geometric principles** underlying the prediction of intraoperative lens touch. It does not substitute for clinical decision-making or patient-specific surgical planning.  

---

## 2. How to Use
1. Enter patient ocular biometry values in the input panel:  
   - Age (years)  
   - AL (Axial Length, mm)  
   - CCT (Central Corneal Thickness, mm)  
   - ACD (Anterior Chamber Depth, mm)  
   - LT (Lens Thickness, mm)  
   - K (Keratometry, diopters)  
   - WTW (White-to-White corneal diameter, mm)  
2. Click **“Calculate Intersection.”**  
3. The results panel will show whether the simulated surgical path intersects the lens at the standardized anatomical risk threshold:  
   - Reference point : 0.71 mm anterior to the equator 
   - If the path intersects the lens, the eye is classified into the high-risk group, indicating a high geometric susceptibility to iatrogenic lens injury.  
   - This single-point assessment identifies cases where the anatomical configuration limits the safety margin for instrument manipulation  
4. A 2D visualization of the eye model is displayed, with annotations for AL, CCT, ACD, LT, WTW, trocar position, and intersection lines.  

---

## 3. Key Notes for Readers and Reviewers
- **Mathematical Basis:**  
  - Corneal radius, lens diameter, and lens radii of curvature are derived using published biometric formulas.  
  - The lens is modeled as intersecting anterior/posterior spherical arcs (Ra/Rp) truncated by the computed lens diameter.  
  - Trocar position is simulated as a chord from limbus to posterior sclera.  

- **Scope:**  
  - The model illustrates the *geometric feasibility* of lens touch during pars plana vitrectomy.  
  - It is a **conceptual and educational tool** only; real intraoperative dynamics (eye movement, surgical angle variability, elasticity) are not included.  

- **Accuracy Considerations:**  
  - Input accuracy depends on measurement precision (e.g., IOLMaster 700).  
  - Extreme values may cause distorted or unstable visualization.  
  - The model assumes a symmetric eye with idealized spherical/elliptical surfaces.  

- **Reproducibility:**  
  - All geometric equations used here correspond directly to the supplementary methods described in the manuscript.  
  - The JavaScript implementation mirrors R code used for the primary analysis.  

---

## 4. Limitations
- Does not model patient-specific scleral thickness, choroid, or dynamic instrument trajectories.  
- Limited to static geometry; real surgery involves variations in angle of attack, indentation, and intraocular pressure.  
- Intended for **scientific communication and transparency** of methods, not for clinical guidance.  

---

## 5. Contact
For questions regarding the model, please contact:  
**Ki Tae Nam, MD**  
Assistant Professor of Ophthalmology  
Jeju National University Hospital / College of Medicine  
Email: *(skarlxo1985@naver.com)*  
