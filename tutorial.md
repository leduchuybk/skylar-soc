1. Checkout sub modules
    ```
    git submodule update --init --recursive
    ```
    * pulp-runtime: a simple sdk
        * Minimal bare-metal runtime
        * Boot-to-main
        * Only uart driver
        * FPGA support
        * Active
    * pulp-runtime-example: examples of pulp-runtime
    * pulpissimo

2. Simulation using simple sdk (pulp-runtime):
    * 2.1. Build target RTL
        * Check out the latest version of the IPs composing the PULP system at pulpissimo folder
        ```
        make checkout
        ```
        This will call ./update-ips and ./generate-scripts script to update ips and to initialize vsim library
        * Build RTL:
        ```
        make build
        ```
        * Source vsim setup
        ```
        source setup/vsim.sh
        ```
    * 2.2. Build pulp-runtime:
        * To use CV32E40P (formely RI5CY) core:
        ```
        cd pulp-runtime
        source configs/pulpissimo.sh
        ```
    * 2.3. Simulation hello example:
        ```
        cd pulp-runtime-examples/hello
        make clean all run # clean and build simulation
        make run gui=1 #open gui
        ```