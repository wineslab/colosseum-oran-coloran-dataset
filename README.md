# Colosseum O-RAN ColORAN Dataset
This repository contains the dataset for the paper M. Polese, L. Bonati, S. D'Oro, S. Basagni, T. Melodia, "ColO-RAN: Developing Machine Learning-based xApps for Open RAN Closed-loop Control on Programmable Experimental Platforms," IEEE Transactions on Mobile Computing, pp. 1-14, July 2022. Please cite the paper if you plan to use it in your publication.

This work was partially supported by the U.S. National Science Foundation under Grants CNS-1923789 and NSF CNS-1925601, and the U.S. Office of Naval Research under Grant N00014-20-1-2132.

## Experiment setup
- Number of Base Stations (BSs): 7
	- Nodes: 1, 8, 15, 22, 29, 36, 43
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
  	- eMBB: Constant bitrate traffic (4 Mbps per UE)
  	- MTC: Poisson traffic (30 pkt/s of 125 bytes per UE)
  	- URLLC: Poisson traffic (10 pkt/s of 125 bytes per UE)
- UEs belong to different traffic classes:
	- eMBB UEs (slice 0): 3, 6, 10, 13, 17, 20, 24, 27, 31, 34, 38, 41, 45, 48
	- MTC UEs (slice 1): 4, 7, 11, 14, 18, 21, 25, 28, 32, 35, 39, 42, 46, 49
 	- URLLC UEs (slice 2): 2, 5, 9, 12, 16, 19, 23, 26, 30, 33, 37, 40, 44, 47
- UEs are divided per slice based on traffic types:
  	- Slice 0: eMBB UEs
  	- Slice 1: MTC UEs
  	- Slice 2: URLLC UEs

## Training configurations
For each scheduling policy (directories [sched0](rome_static_medium/sched0), [sched1](rome_static_medium/sched1), [sched2](rome_static_medium/sched2)), the Resource Block Group (RBG) allocations for each slice are as follows.

<table>
<thead>
<tr>
<th></th>
<th align="center" colspan="3">Number of RBGs per Slice</th>
</tr>
</thead>
<thead>
<tr>
<th align="center">Training</th>
<th align="center">Slice 0</th>
<th align="center">Slice 1</th>
<th align="center">Slice 2</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">tr0</td>
<td align="right">2</td>
<td align="right">13</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr1</td>
<td align="right">4</td>
<td align="right">11</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr2</td>
<td align="right">6</td>
<td align="right">9</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr3</td>
<td align="right">8</td>
<td align="right">7</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr4</td>
<td align="right">10</td>
<td align="right">5</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr5</td>
<td align="right">12</td>
<td align="right">3</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr6</td>
<td align="right">14</td>
<td align="right">1</td>
<td align="right">2</td>
</tr>
<tr>
<td align="right">tr7</td>
<td align="right">2</td>
<td align="right">11</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr8</td>
<td align="right">4</td>
<td align="right">9</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr9</td>
<td align="right">6</td>
<td align="right">7</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr10</td>
<td align="right">8</td>
<td align="right">5</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr11</td>
<td align="right">10</td>
<td align="right">3</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr12</td>
<td align="right">12</td>
<td align="right">1</td>
<td align="right">4</td>
</tr>
<tr>
<td align="right">tr13</td>
<td align="right">2</td>
<td align="right">9</td>
<td align="right">6</td>
</tr>
<tr>
<td align="right">tr14</td>
<td align="right">4</td>
<td align="right">7</td>
<td align="right">6</td>
</tr>
<tr>
<td align="right">tr15</td>
<td align="right">6</td>
<td align="right">5</td>
<td align="right">6</td>
</tr>
<tr>
<td align="right">tr16</td>
<td align="right">8</td>
<td align="right">3</td>
<td align="right">6</td>
</tr>
<tr>
<td align="right">tr17</td>
<td align="right">10</td>
<td align="right">1</td>
<td align="right">6</td>
</tr>
<tr>
<td align="right">tr18</td>
<td align="right">2</td>
<td align="right">7</td>
<td align="right">8</td>
</tr>
<tr>
<td align="right">tr19</td>
<td align="right">4</td>
<td align="right">5</td>
<td align="right">8</td>
</tr>
<tr>
<td align="right">tr20</td>
<td align="right">6</td>
<td align="right">3</td>
<td align="right">8</td>
</tr>
<tr>
<td align="right">tr21</td>
<td align="right">8</td>
<td align="right">1</td>
<td align="right">8</td>
</tr>
<tr>
<td align="right">tr22</td>
<td align="right">2</td>
<td align="right">5</td>
<td align="right">10</td>
</tr>
<tr>
<td align="right">tr23</td>
<td align="right">4</td>
<td align="right">3</td>
<td align="right">10</td>
</tr>
<tr>
<td align="right">tr24</td>
<td align="right">6</td>
<td align="right">1</td>
<td align="right">10</td>
</tr>
<tr>
<td align="right">tr25</td>
<td align="right">2</td>
<td align="right">3</td>
<td align="right">12</td>
</tr>
<tr>
<td align="right">tr26</td>
<td align="right">4</td>
<td align="right">1</td>
<td align="right">12</td>
</tr>
<tr>
<td align="right">tr27</td>
<td align="right">2</td>
<td align="right">1</td>
<td align="right">14</td>
</tr>
</tbody>
</table>
