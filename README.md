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

Extra: Often EBSD data is formated specific to the detector and software package used for measurement. 
For this reason, it can be difficult to transfer data from one system to another. 
Especially for HREBSD, in which patterns are stored in seperate files for Edax systems, 
it is necessay to reformat the file types to be accessible in other tools like Aztec Crystal. 
