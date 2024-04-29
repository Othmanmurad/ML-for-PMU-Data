# pmuBAGE
This is a repository for the synthetic phasor measurement unit dataset pmuBAGE. (The Benchmarking Assortment of Generated PMU Events). See our [paper]( https://arxiv.org/abs/2204.01095) for details - and please cite this paper if you use the dataset!

Sample synthetic frequency event and voltage event figures are shown below.

<img src="https://github.com/NanpengYu/pmuBAGE/blob/main/images/gf.png" width="300" height="500"><img src="https://github.com/NanpengYu/pmuBAGE/blob/main/images/gv.png" width="300" height="500">

The dataset consists of 84 synthetic frequency events and 620 synthetic voltage events. It is split into several partitions, all found in the "data" subdirectory. Frequency events are partitioned into 21 tensors each consisting of 4 events, and the voltage events are partitioned into 31 tensors each consisting of 20 events. Each NumPy tensor in these subdirectories is 4 dimensional. The dimensions are described as follows:

1. The event axis. Each index on this axis corresponds to a unique synthetic event.
2. The datatype axis (PQVF). The first index of this axis corresponds to real power, the second to reactive power, the third to voltage magnitude, and the fourth to frequency. 
3. The PMU axis. Each index corresponds to a different synthesized synchrophasor. There are 100 indices on this axis.
4. The temporal axis. Each index corresponds to a different timestamp. There are 600 indices on this axis (20 seconds)

Each frequency event tensor file has size 4x4x100x600, and eachv oltage event tensor file has size 20x4x100x600
