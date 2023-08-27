# davis-alveo-u280
Repo for collaboration using the Alveo U280

Refer to https://users.ece.utexas.edu/~mcdermot/arch/articles/Zynq/pg021_axi_dma.pdf page 72 "Programming sequence" for what this module does.

Upon pulsing the init_tx signal (set high for a single cycle), the DMA controller will attempt to program the DMA for simple (not scatter gather) S2MM and MM2S behavior and start it.

The configuration settings are currently hardcoded into the core. This is temporary.

It is set up to read a 16 byte message from x1_0000_1000 and write it to x1_0000_2000.

It is currently non-cyclical, or at least it hasn't been tested. It just runs once.

This controller has been tested and validated with a DMA connected to a BRAM. 
