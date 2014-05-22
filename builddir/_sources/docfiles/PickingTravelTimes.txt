Measuring Teleseismic Body Wave Arrival Times
=============================================

The core idea in using AIMBAT to measure teleseismic body wave arrival times has two parts: 
* automated phase alignment, to reduce user processing time, and
* interactive quality control, to retain valuable user inputs.

Automated Phase Alignment
-------------------------

The ICCS algorithm calculates an array stack from predicted time picks, cross-correlates each seismogram with the array stack to Find the time lags at maximum cross-correlation, then use the new time picks to update the array stack in an iterative process. The MCCC algorithm cross-correlates each possible pair of seismograms and uses a least-squares method to calculate an optimized set of relative arrival times. Our method is to combine ICCS and MCCC in a four-step procedure using four anchoring time picks :math:`_0T_i,\,_1T_i,\,_2T_i,` and :math:`_3T_i`.

(a) Coarse alignment by ICCS
(b) Pick phase arrival at the array stack
(c) Refined alignment by ICCS
(d) Final alignment by MCCC

The one-time manual phase picking at the array stack in step (b) allows the measurement of absolute arrival times. The detailed methodology and procedure can be found in [LouVanDerLee2013]_.

.. table:: Time picks and their SAC headers used in the procedure for measuring teleseismic body wave arrival times.

	+------+-----------+-------------+----------------+-------------+---------------+-------------+
	| Step | Algorithm |                    Input                   |            Output           |
	+      +           +-------------+----------------+-------------+---------------+-------------+
	|      |           | Time Window | Time Pick      | Time Header | Time Pick     | Time Header |
	+------+-----------+-------------+----------------+-------------+---------------+-------------+
	| (a)  |   ICCS    | :math:`W_a` | :math:`_0T_i`  | **T0**      | :math:`_1T_i` | **T1**      |     
	+------+-----------+-------------+----------------+-------------+---------------+-------------+
	| (b)  |   ICCS    | :math:`W_b` | :math:`_2T'_i` | **T2**      | :math:`_2T_i` | **T2**      |     
	+------+-----------+-------------+----------------+-------------+---------------+-------------+
	| (d)  |   MCCS    | :math:`W_b` | :math:`_2T_i`  | **T2**      | :math:`_3T_i` | **T3**      |     
	+------+-----------+-------------+----------------+-------------+---------------+-------------+

