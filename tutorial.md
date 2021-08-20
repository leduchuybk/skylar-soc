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

2. Build pulp-runtime:
    * Go into pulp-runtime folder
    * To use CV32E40P (formely RI5CY) core:
    ```
    source configs/pulpissimo.sh
    ```

3. Simulation using simple sdk (pulp-runtime):
    * Check out the latest version of the IPs composing the PULP system at pulpissimo folder
    ```
    make checkout
    ```
    This will call ./update-ips and ./generate-scripts script to initialize vsim library
    * Build RTL:
    ```
    make build
    ```
    * Source vsim setup
    ```
    source setup/vsim.sh
    ```

5. Simulation hello example:
    ```
    cd pulp-runtime-examples/hello
    make clean all run # clean and build simulation
    make run gui=1 #open gui
    ```