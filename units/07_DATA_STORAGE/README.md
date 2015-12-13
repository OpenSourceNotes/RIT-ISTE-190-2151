# ISTE-190 - Data Storage

## Two technologies
* Magnetic disk drives (HDD)
* Solid state drives (SSD)

## Magnetic disk drives (HDDs)
* Mature technology, but may have reached maximum point of growth
* Extraordinary engineering - moving parts with very small fault tolerances
* Structure
 * Magnetized data on disk
 * Tracks in disk (75nm track width)
 * Disk is rotating
 * Head reads data from disk; moves back and forth to read data
* 4TB drive = $140, or $0.035/GB

### Rotational speed
* 15000 rpm (enterprise / high-end server class)
* 7200 rpm (PC class)
* 5400 rpm (PC class)
* *Latency*: Average half-rotation until data is under read/write heads
 * 15000 rpm: 2ms
 * 7200 rpm: 4ms
 * 5400 rpm: 5.5ms
* Average seek time for read/write head: ~3ms (server class)

### CPU comparison
* Eternity at CPU level
* Total time to read or write data to HDD =
 * Latency time +
 * Seek time +
 * Data transfer from disk to main memory (300-600MB/sec) sustained rate (burst rate higher)
* Server Class: 2ms + 3ms + data transfer rate = 5ms + transfer time
* Effective read speeds can be improved by cache memory integrated into disk controller

### Reliability
* Always concern with moving parts
* Read and write at high densities means read/write heads fly very close to platter's surface
 * Range of 3-10 nanometers (an engineering feat)
 * Current transistor technology at 14-22 nanometers
* Size of dust and smoke particles larger than flying height of read/write heads
 * Potential for head crash
![Crash!](https://i.j-f.co/u/04ad9afb1a3c0ab4b940f4fe6e8c7848.png)

## Solid state drives (SSDs)
* All transistors
 * No moving partsx
* Advantages over HDD
 * Faster read time (about order of magnitude faster)
 * Higher reliability
 * Less power (and less heat)
* Disadvantages
 * More expensive (0.5 - 1 order of magnitude more expensive)

## HDD vs. SSD
* Seagate, leading HDD manufacturer, disk capacity will increase from 4TB in 2013 to 60TB in 2020
* HDD technology will maintain cost advantage into foreseeable future
* SSD technology will maintain perforamnce advantage into foreseeable future

## Storage at scale
* Locally attached disk to each cluster compute node
* Pools of storage accessible over a storage area network (SAN)
 * Clusters
 * Mainframes
* Hybrid approach: Uses both HDD and SSD
 * SSD can be used as cache memory for HDD
* Many automatic system management capabilities