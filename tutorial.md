1. Checkout pulpissimo (branch: my_pulpissimo)
    ```
    git submodule update --init --recursive
    ```
2. Checkout pulp-sdk and pulp-runtime* folders in pulpissimo
    ```
    git submodule update --init --recursive
    ```
    pulp-sdk: a complete sdk
    pulp-runtime: a simple sdk
    pulp-runtime-example: examples

3. Build pulp-runtime:
    * Go into pulp-runtime folder
    * To use CV32E40P (formely RI5CY) core:
    ```
    source configs/pulpissimo.sh
    ```
4. Simulation using simple sdk (pulp-runtime):
    * Check out the latest version of the IPs composing the PULP system at pulpissimo folder
    ```
    make checkout
    ```
    This will call ./update-ips and ./generate-scripts script to initialize vsim library
    * Build RTL:
    ```
    make build
    ```