# EdaxToAztec
Converts EDAX .osc (orientations) in Binary + .UP2 (patterns) into an AZtec-style HDF5 (H5OINA-like) file.  
Usage: python edax_to_aztec_h5.py --osc path/to/file.osc --up2 path/to/file.UP2 --out merged.h5  

Notes:

Designed to stream patterns to HDF5 to handle large datasets.
Attempts to auto-detect OSC column layout; fallback assumptions are provided.
For unusual EDAX variants, tweak the osc_column_map or header offsets.

Requirements: 
EBSD Grids must be set to Square and not Hex.
Resolution of the acquistion must be known. (1x1 binning at 480 x 480)

