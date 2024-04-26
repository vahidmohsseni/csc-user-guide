---
tags:
  - Free
---

# Octave
GNU Octave is a high-level interpreted language, primarily intended for numerical computations.
It provides capabilities for the numerical solution of linear and nonlinear problems, and for performing other numerical experiments.
It also provides extensive graphics capabilities for data visualization and manipulation.
Octave is normally used through its interactive command line interface, but it can also be used to write non-interactive programs.
The Octave language is quite similar to Matlab so that most programs are easily portable.

[TOC]


## License
Octave is licensed under the open-source, GNU General Public License (GPL).


## Available
Octave 9.1.0 is available on Puhti and Mahti.


## Usage
### Interactive use on Puhti
You can use Octave by the loading the module:

```bash
module load octave
```

Then, start Octave with the command:

```bash
octave
```

Octave is installed as a container.


## Installing packages
You can install [Octave packages](https://packages.octave.org/) on the user side as follows:

```octave
pkg install -local "<pkg-url>"
```

If you need to install a package that require Linux packages, you can send a message to the Service Desk and we will install them to the container.


### Example batch jobs
Example about a serial batch script job on Puhti

```bash
#!/bin/bash
#SBATCH --account=<project>
#SBATCH --partition=small
#SBATCH --time=00:15:00
#SBATCH --nodes=1
#SBATCH --ntasks-per-node=1
#SBATCH --cpus-per-task=1
#SBATCH --mem-per-cpu=1000

module load octave
srun octave script.m
```

Submit the script with `sbatch <script_name.sh>`


<!--
## References
In view of the many contributions made by numerous developers over many years it is common courtesy to cite Octave in publications when it has been used during the course of research or the preparation of figures. The citation function can automatically generate a recommended citation text for Octave or any of its packages. See the help text below on how to use citation.

```bash
> citation
> citation <package>
```

Above commands will display instructions for citing GNU Octave or its packages in publications. When called without an argument, display information on how to cite the core GNU Octave system. When given a package name package, display information on citing the specific named package. Note that some packages may not yet have instructions on how to cite them.
-->
