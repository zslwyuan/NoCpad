Header files:
- `src/include/arbiters.h` HLS implementation of various arbitration schemes
- `src/include/axi4_configs_extra.h` Expansion of Matclib's AXI configuration
- `src/include/dnp20_axi.h` definitions of packetization structure
- `src/include/duth_fun.h` helper low-level HLS functions commonly used
- `src/include/flit_axi.h` Network flit class that transports AXI
- `src/include/onehot.h` Onehot wrapped class to introduce onehot representation  
- `src/include/fifo_queue_oh.h` An onehot FIFO implementation

Routers:
- `src/router_wh.h` Wormhole router implementation
- `src/router_vc.h` Virtual Channel based router similar to combined allocation paradigm of [Microarchitecture of Network-on-Chip Routers](https://www.springer.com/gp/book/9781461443001)

Interfaces:
- `src/axi_master_if.h` Master interface that connects the Master agent to the network, capable of multiple outstanding transactions under two schemes, towards the same transaction destination, and towards multiple detinations for transactions of different IDs
- `src/axi_master_if_reord.h` Master interface that connects the Master agent to the network, with out-of-order outstanding requests and reordering capabilities to maintain AXI ordering
- `src/axi_slave_if.h` Slave interface that connects the Slave agent to the network

- `src/axi_master_if_vc.h` Master interface that connects the Master agent to the network, capable of multiple outstanding transactions under two schemes. Supports Virtual Channels.
- `src/axi_master_if_vc_reord.h` Master interface that connects the Master agent to the network, with reordering capabilities and Virtual Channel based Network-on-Chip support.
- `src/axi_slave_if_vc.h` Slave interface that connects the Slave agent to the network that supports Virtual Channel based Network-on-Chip