# Fibrosis Staging Tool — English version

Static site intended for GitHub Pages and embedding in Google Sites.

## Deployment

Upload `index.html`, `app.js`, and `models.json` to the root of your GitHub Pages repository. Keep all three files together. Enable GitHub Pages under Settings → Pages. In Google Sites, select Insert → Embed → By URL and paste the published GitHub Pages URL.

## Model behavior

This release translates the user interface into English **without changing the predictive models or calculation logic** from version 4. The application calculates standard FIB-4 as `AGE * AST / (PL * sqrt(ALT))`, including derived features used during inference, while retaining the original exported decision-tree and LDA coefficients.

The tool supports GLOBAL, HBV, HCV, HBCV and MASLD datasets, each with decision tree and decision tree + LDA methods. Classes: G1 (F0–F1) and G2 (F2–F4).

No patient data are transmitted to a prediction API. The tool is intended as research support and does not replace clinical assessment.
