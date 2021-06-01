# trim_beam.py
<i>Python3 script to trim or rebuild an Apertif spectral line beam cube</i>

Simple python3 script to reduce the size of an Apertif spectral line beam
cube by a factor 2 by cutting the beams in half in x.  It assumes that
the beams have the standard size of 1321 x 1321 x nchan and reduces
them to 661 x 1321 x nchan by omitting all values from x = 6612 - 1321.
The full beams can be reconstructed by mirroring the values of the
halved beam from x = 1 - 660 and pad these at x = 662 - 1321.
nchan must be larger than 1.

The script is run as 
"<b>local_path/trim_beam.py  input_beam  output_beam  nr</b>"

where nr = -1 for trimming and nr = +1 for
rebuilding the beam.  The file format used is FITS.

The first line in the script must then be changed to point to your
local python3 installation and the script must be made executable with
"<b>chmod +x trim_beam.py</b>"
  
Alternatively one can run the script as 
"<b>python3  local_path/trim_beam.py  input_beam  output_beam  nr</b>"


