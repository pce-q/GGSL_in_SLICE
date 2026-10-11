Light models for SPT-CLJ0549-6205 (The Archer)
==============================================

Layout
------
prepared_<tag>/<band>/
  data.fits       cutout image
  rms.fits        per-pixel 1σ noise (for residual/σ)
  arcs_mask.npy   True = masked (arcs / unrelated)

fits_<tag>/<band>_<method>/
  model.fits      total model image (same WCS/grid as data)
  model_*.fits    optional components (hybrid / MGE)
  half_light_ellipses.csv   (hybrid tags) true Re ellipses

figures/
  <tag>/          subtraction / quicklook PNGs for that model
  archer_hybrid_hardlock_presub_subtracted.png   adopted paper figure

Minimal visualisation (Python)
------------------------------
  data  = fits.getdata(f"prepared_<tag>/<band>/data.fits")
  model = fits.getdata(f"fits_<tag>/<band>_*/model.fits")
  rms   = fits.getdata(f"prepared_<tag>/<band>/rms.fits")
  resid = (data - model) / rms

Adopted science model: hybrid_mge_ds_hardlock_presub
