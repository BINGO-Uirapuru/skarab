# SKARAB

**SKARAB** is an agile, networked, FPGA-centric cluster computing or instrument node. The Square Kilometre Array Reconfigurable Application Board (SKARAB) is the latest generation of CASPER FPGA hardware. It is the next generation/successor to the ROACH2 platform.

# BINGO

The *BINGO* Project aims at building a special purpose radio telescope to map redshifted neutral hydrogen emission between z = 0.13 and 0.45.

*BINGO* stands for **B**aryon Acoustic Oscillations from **I**ntegrated **N**eutral **G**as **O**bservations.

It is an international project with collaborators in Brazil, China, United Kingdom, France, South Africa, Germany, and United States. It is the only radio telescope that proposes mapping neutral gas as traced by the 21cm line on large angular scales at redshift z~0.3.

# Application

The BINGO project uses the skarab to process the data read by the antenna before sending it to the server for further processing and database saving. 

# Install toolflow

## *casperfpga* from pip (for ubuntu >=20.04)

Get the installed python version on your computer:

    python3 --version

And follow the install guide to download miniconda accordingly to your python version from the [link](https://docs.conda.io/en/latest/miniconda.html)

After the installation has ended, create a python 2.7 environment with:

    conda create -n cfpga_venv python=2.7

If you don't what the conda initiating the environment in every new terminal window, use this config:

    conda config --set auto_activate_base false

Activate the python 2.7 environment

    conda activate cfpga_venv

Install the casperfpga python package and the ipython for testing

    pip install casperfpga ipython

Turn on the Skarab and test with

```python
import casperfpga

skarab = caspfpga.CasperFpga('xxx.xxx.xxx.xxx')

skarab.upload_to_ran_and_program('file_path.fpg')
```

# Reference

* [Casper toolflow docs](https://casper-toolflow.readthedocs.io/en/latest/index.html)
* [Casper toolflow repo](https://github.com/casper-astro/mlib_devel)
* [Casper hardware list](https://github.com/casper-astro/casper-hardware)
* [casperfpga github](https://github.com/ska-sa/casperfpga)
* [SKARAB BSP images](https://github.com/ska-sa/skarab_bsp_images)
* [SKARAB microprocessor](https://github.com/ska-sa/skarab_microblaze_software)
* [SKARAB LED manager](/SKARAB_LED_Manager.pdf)