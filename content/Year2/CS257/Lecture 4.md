## Interleaved Memory

- Makes access fast with concurrency, since the consecutive words are in separate banks

***Example:*** No interleaving means only one thread can be used to read off memory, due to concurrency issues mentioned in [[Year2/CS241/Content/Module Details|CS241]] (tl;dr: one writeable resource can only be used by one thread at a time). This is quite slow.
- *To me:* is thread the right term for this?

**Solution:** Having 2 banks means that 2 threads can read off memory, since each thread can grab the data from its own assigned bank.

Note about the lecture diagram (paste in later?): diagram is for a 4-bank interleaved memory model. Arrows only drawn for the first 2 banks which makes it confusing 


## Synchronous DRAM (SDRAM)

With DRAM, slow access times due to waiting for data to become available. 

With SDRAM, external clock that runs near speed of processor -> SDRAM exchanges data on clock with processor.

## Double Data Rate SDRAM (DDR SDRAM)

## Rank and Module

- Energy inefficient? 

## Static RAM (SRAM) 

*Cache Level (External Cache)*

- Volatile data *but* does not require refresh cycle 
	- Power must be continually applied (since volatile)

### SRAM vs DRAM

DRAM cells are simpler & more compact 
- way cheaper
- greater cell density
- refresh circuitry incurs one-off cost (?)

SRAM has: 

### Embedded DRAM (eDRAM)

In between SRAM and DRAM.

- DRAM integrated on same chip or MCM of an ASIC or microprocessor


