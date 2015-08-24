
# Gr-osmosdr SDRplay Patch

This patch corrects a bug that affects
the proper reading of samples from the SDRplay.
The current gr-osmosdr library incorrectly considers 
SDRplay samples as right justified. 
The patch corrects the code to read the samples as left justified.

The patch also changes the way the gr-osmosdr library calculates 
the bandwidth setting for the SDRplay.  Before the patch, setting
the bandwidth to 2 MHz would actually set the bandwidth to
5 MHz.  Now the bandwidth is set to 1.536 MHz instead.

To apply the patch, you can use:

     git apply gr-osmosdr.sdrplay.diff



