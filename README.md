# Layout Optimization for a Large-Scale Grid-Connected Solar Power Plant
This repository contains supplementary materials for the review of the paper "Layout Optimization for a Large-Scale Grid-Connected Solar Power Plant".

## Data
The folder [data](data) contains instances originally collected from the Hubei Branch of the [State Grid Corporation of China](http://www.sgcc.com.cn/html/sgcc_main_en/index.shtml). All sensitive or confidential information has been appropriately desensitized.

Each instance (denoted by "district_<span>$a$</span>-<span>$b$</span>") represents a grid-connected solar power plant with a set of photovoltaic arrays (PVAs) continuously placed in a PV farm. Here, $a$ is the number of districts, and $b$ is an index representing different layout shapes. Each district in these plants has 109 slots of PVAs, one of which is removed to install an inverter. 

Each PNG file "district_<span>$a$</span>-<span>$b$</span>.png" illustrates the placement of PVAs, where the partitioning result is obtained by our Heuristic Search algorithm, and the blue dotted line represents the induced inner cut edges.

Each TXT file "district_<span>$a$</span>-<span>$b$</span>.txt" provides information about the location of PVAs, with each line reporting the index, x-coordinate, y-coordinate, and district to which a PVA is asssinged.

The length parameters are provided in meters. The distance between two PVAs is measured by the Manhattan distance (L1 norm).  The potential service ways can be built by traversing the entire farm between any two consecutive PVA columns. The length of a service way is calculated as $8.500 \times max(n^{1},n^{2})$, where $n^{1}$ and $n^{2}$ are respectively the number of PVAs located along the two adjacent columns of this service way.

The cost parameters are provided in USD. The cabling cost for connecting a combiner box to the inverter is $c_1 = 10.904$ per meter and that for connecting a PVA to a combiner box is $c_2 = 3.937$ per meter. The cost for building a service way is $46.312$ 
per meter. Two types of combiner box ($T=2$), each with capacity $p_1=6$ and $p_2 =8$, are used in these plants and their purchasing costs $g_1 = 94.476$ and $g_2 = 110.222$, respectively.
