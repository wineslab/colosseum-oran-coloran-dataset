# Colosseum ColoRAN O-RAN Dataset
This repository contains the dataset for the paper M. Polese, L. Bonati, S. D'Oro, S. Basagni, T. Melodia, "ColoRAN: Design and Testing of Open RAN Intelligence on Large-scale Experimental Platforms," arXiv XXX, December 2021. Please cite the paper if you plan to use it in your publication.

## Experiment setup
- Number of Base Stations (BSs): 7
- Channel bandwidth: 10 MHz (50 Physical Resource Blocks (PRBs))
- Number of slices for each BS: 3
- Scheduling policies available to each slice:
	- Policy 0: Round-robin (RR)
  - Policy 1: Waterfilling (WF)
  - Policy 2: Proportionally fair (PF)
- Number of User Equipments (UEs): 42
- Radio Frequency (RF) scenario setup (Colosseum Rome scenario):
  	- Medium: UEs uniformly distributed within 50 m of each BS
- UE Mobility: static
- Traffic classes:
  	- eMBB: Constant bitrate traffic (1 Mbps per UE)
  	- MTC: Poisson traffic (30 pkt/s of 125 bytes per UE)
  	- URLLC: Poisson traffic (10 pkt/s of 125 bytes per UE)
- UEs belong to different traffic classes:
  	- eMBB UEs (slice 0): 3, 6, 9, 14, 17, 20, 25, 28, 31, 36, 39, 42
  	- MTC UEs (slice 1): 4, 7, 10, 15, 18, 21, 26, 29, 32, 37, 40, 43
  	- URLLC UEs (slice 2): 2, 5, 8, 11, 13, 16, 19, 22, 24, 27, 30, 33, 35, 38, 41, 44
- UEs are divided per slice based on traffic types:
  	- Slice 0: eMBB UEs
  	- Slice 1: MTC UEs
  	- Slice 2: URLLC UEs

## Training configurations
The scheduling policies and initial Resource Block Group (RBG) allocations for each slice are as follows.

<table>
<thead>
<tr>
<th></th>
<th align="center" colspan="3">Slice Scheduling Policy</th>
<th align="center" colspan="3">Slice RBG Allocation</th>
</tr>
</thead>
<thead>
<tr>
<th align="center">Training</th>
<th align="center">Slice 0</th>
<th align="center">Slice 1</th>
<th align="center">Slice 2</th>
<th align="center">Slice 0</th>
<th align="center">Slice 1</th>
<th align="center">Slice 2</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">tr0</td>
<td align="right">PF</td>
<td align="right">RR</td>
<td align="right">PF</td>
<td align="right">1</td>
<td align="right">2</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr1</td>
<td align="right">WF</td>
<td align="right">RR</td>
<td align="right">RR</td>
<td align="right">1</td>
<td align="right">4</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr2</td>
<td align="right">RR</td>
<td align="right">PF</td>
<td align="right">WF</td>
<td align="right">2</td>
<td align="right">1</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr3</td>
<td align="right">WF</td>
<td align="right">WF</td>
<td align="right">PF</td>
<td align="right">2</td>
<td align="right">4</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">tr4</td>
<td align="right">RR</td>
<td align="right">WF</td>
<td align="right">WF</td>
<td align="right">4</td>
<td align="right">2</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">tr5</td>
<td align="right">WF</td>
<td align="right">WF</td>
<td align="right">WF</td>
<td align="right">4</td>
<td align="right">1</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr6</td>
<td align="right">PF</td>
<td align="right">PF</td>
<td align="right">WF</td>
<td align="right">2</td>
<td align="right">2</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">tr7</td>
<td align="right">WF</td>
<td align="right">RR</td>
<td align="right">PF</td>
<td align="right">2</td>
<td align="right">3</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr8</td>
<td align="right">WF</td>
<td align="right">PF</td>
<td align="right">RR</td>
<td align="right">3</td>
<td align="right">2</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr9</td>
<td align="right">PF</td>
<td align="right">WF</td>
<td align="right">RR</td>
<td align="right">3</td>
<td align="right">3</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">tr10</td>
<td align="right">RR</td>
<td align="right">RR</td>
<td align="right">PF</td>
<td align="right">3</td>
<td align="right">1</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">tr11</td>
<td align="right">RR</td>
<td align="right">PF</td>
<td align="right">RR</td>
<td align="right">1</td>
<td align="right">3</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">tr12</td>
<td align="right">RR</td>
<td align="right">RR</td>
<td align="right">RR</td>
<td align="right">1</td>
<td align="right">2</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr13</td>
<td align="right">WF</td>
<td align="right">PF</td>
<td align="right">WF</td>
<td align="right">1</td>
<td align="right">4</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr14</td>
<td align="right">PF</td>
<td align="right">WF</td>
<td align="right">PF</td>
<td align="right">4</td>
<td align="right">2</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">tr15</td>
<td align="right">RR</td>
<td align="right">WF</td>
<td align="right">PF</td>
<td align="right">3</td>
<td align="right">1</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr16</td>
<td align="right">PF</td>
<td align="right">RR</td>
<td align="right">RR</td>
<td align="right">1</td>
<td align="right">2</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr17</td>
<td align="right">PF</td>
<td align="right">RR</td>
<td align="right">WF</td>
<td align="right">1</td>
<td align="right">2</td>
<td align="right">4</td>
</tr>
</tbody>
</table>

## Dynamic slice resizing
After the initial allocation, the RBGs for each slice are dynamically re-allocated as follows.

<table>
<thead>
<tr>
<th align="center">Time [s]</th>
<th align="center">RBG Slice 0</th>
<th align="center">RBG Slice 1</th>
<th align="center">RBG Slice 2</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">0-30</td>
  <td align="center" colspan="3">initial allocation (see training configurations above)</td>
</tr>
<tr>
<td align="right">30-60</td>
<td align="right">1</td>
<td align="right">2</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">60-90</td>
<td align="right">1</td>
<td align="right">4</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">90-120</td>
<td align="right">2</td>
<td align="right">1</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">120-150</td>
<td align="right">2</td>
<td align="right">4</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">150-180</td>
<td align="right">4</td>
<td align="right">2</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">180-210</td>
<td align="right">4</td>
<td align="right">1</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">210-240</td>
<td align="right">2</td>
<td align="right">2</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">240-270</td>
<td align="right">2</td>
<td align="right">3</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">270-300</td>
<td align="right">3</td>
<td align="right">2</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">300-330</td>
<td align="right">3</td>
<td align="right">3</td>
<td align="right">1</td>
</tr>
<tr>
<td align="right">330-360</td>
<td align="right">3</td>
<td align="right">1</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">360-390</td>
<td align="right">1</td>
<td align="right">3</td>
<td align="right">3</td>
</tr>
<tr>
<td align="right">390-420</td>
<td align="right">1</td>
<td align="right">2</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">420-450</td>
<td align="right">1</td>
<td align="right">4</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">450-480</td>
<td align="right">4</td>
<td align="right">2</td>
<td align="right">1</td>
</tr>
</tbody>
</table>