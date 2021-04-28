# trim_beam.py
Python3 script to trim or rebuild Apertif spectral line cube

Simple python3 script to reduce the size of an Apertif spectral line 
cube by a factor 2 by cutting the beams in half in x.
It assumes that the beams have the standard size of 1321 x 1321 x 1218
and reduces them to 661 x 1321 x 1218 by omitting all values from
x = 6612 - 1321.
The full beams can be reconstructed by mirroring the values of the 
halved beam from x = 1 - 660 and pad these at x = 662 - 1321.

The script is run as "./trim_beam input_beam output_beam nr" 
where nr = -1 for trimming and nr = +1 for rebuilding the beam.
The file format used is FITS.
