[![CircleCI](https://dl.circleci.com/status-badge/img/gh/fusion-energy/neutronics-workshop/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/fusion-energy/neutronics-workshop/tree/main)
[![CI with install](https://github.com/fusion-energy/neutronics-workshop/actions/workflows/ci_tests.yml/badge.svg)](https://github.com/fusion-energy/neutronics-workshop/actions/workflows/ci_tests.yml)

[![docker-publish-release](https://github.com/fusion-energy/neutronics-workshop/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/fusion-energy/neutronics-workshop/actions/workflows/docker-publish.yml)

# Fusion Neutronics workshop
A selection of resources for learning fusion neutronics simulations with a
particular focus on OpenMC with DAGMC and the Paramak

There is a 
[slide](https://slides.com/neutronics_workshop/neutronics_workshop) deck that introduces
the workshop and show the expected outputs of each task.

The use of [OpenMC](https://openmc.org/), [DAGMC](https://svalinn.github.io/DAGMC/)
and [Paramak](https://paramak.readthedocs.io) for neutronics analysis requires
several software packages and nuclear data.
These have all been installed inside a Docker container.
The video below gives a brief explainer of what to expect in the workshop and
some motivation for learning neutronics.

The neutronics workshop was created by and is maintained by
[Jonathan Shimwell](https://github.com/shimwell/).
The repository has benefited greatly from contributions from [John Billingsley](https://github.com/billingsley-john)
and [others](https://github.com/fusion-energy/neutronics-workshop/graphs/contributors)

The resource has proven most useful as it is one of the few open source and
accessible fusion neutronics training resources.

The repository has benefited greatly from user feedback. Please feel free to
raise Github [issues](https://github.com/fusion-energy/neutronics-workshop/issues)
or reach out in the [discussions](https://github.com/fusion-energy/neutronics-workshop/discussions)
section if you spot anything that needs fixing or think of an improvement.
Contributions are also very welcome as pull requests to the develop branch.

<p align="center"><a href="https://youtu.be/HH-poTG-FxM" target="_blank"><img src="https://user-images.githubusercontent.com/8583900/144746742-3e31e0ee-6380-4db7-b8ea-0b1c302d497b.png" height="400" /></a></p>

<!-- # Run in the cloud (low CPU count)

One advantage of the containerization of the entire software stack is that it
can be deployed in the cloud and launched in your browser on demand.

To demonstrate this I've deployed the workshop on a minimal cloud computer which
can be spun up by anyone going to the following URL.
This is mainly intended for demonstration purposes and the CPU count is low to
keep my costs down.
For the the best performance there are other options for deployment which take
more effort than clicking a link but provide more computing power.
:point_right: [Try the workshop in your browser](https://neutronics-workshop-4zf6u4tg6a-lz.a.run.app/) -->

<!-- # Run in the cloud (higher CPU count) -->

# Local Installation

There are video tutorials for this section which accompany the step by step
instructions below.
- Ubuntu installation video :point_right: <p align="center"><a href="https://youtu.be/qJLmt_dAaC0" target="_blank"><img src="https://user-images.githubusercontent.com/8583900/114008054-c9cb7e80-9859-11eb-8e07-32e95c600667.png" height="70" /></a></p>
- Windows installation video :point_right: <p align="center"><a href="https://youtu.be/1MUYgjEQeIA" target="_blank"><img src="https://user-images.githubusercontent.com/8583900/114008108-d3ed7d00-9859-11eb-8bb5-0c19ce775015.png" height="70" /></a></p>
- Mac installation video :point_right: <p align="center"><a href="https://youtu.be/jUMY-cEILcw" target="_blank"><img src="https://user-images.githubusercontent.com/8583900/114172031-05834880-992d-11eb-8277-5a6cda2b5e12.png" height="70" /></a></p>

1. Install Docker CE for
[Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/),
[Mac OS](https://store.docker.com/editions/community/docker-ce-desktop-mac), or
[Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows),
including the part where you enable docker use as a non-root user. 

2. Pull the docker image from the store by typing the following command in a
terminal window, or Windows users might prefer PowerShell.

    ```docker pull ghcr.io/fusion-energy/neutronics-workshop```

    <details>
      <summary><b>Expand</b> - Having permission denied errors?</summary>
        <pre><code class="language-html">
        If you are running the command from Linux or Ubuntu terminal and getting permission denied messages back.
        Try running the same command with with elevated user permissions by adding sudo at the front.
        sudo docker pull ghcr.io/fusion-energy/neutronics-workshop
        Then enter your password when prompted.
        </code></pre>
    </details>

3. Now that you have the docker image you can enable graphics linking between
your os and docker, and then run the docker container by typing the following
commands in a terminal window.

    ```docker run -p 8888:8888 ghcr.io/fusion-energy/neutronics-workshop```

    <details>
      <summary><b>Expand</b> - Having permission denied errors?</summary>
        <pre><code class="language-html">
        If you are running the command from Linux or Ubuntu terminal and getting permission denied messages back.
        Try running the same command with with elevated user permissions by adding sudo at the front.
        sudo docker run -p 8888:8888 ghcr.io/fusion-energy/neutronics-workshop
        Then enter your password when prompted.
        </code></pre>
    </details>

4. A URL should be displayed in the terminal and can now be opened in the
internet browser of your choice. Select and open the URL at the end of the terminal print out (highlighted below)

<p align="center"><img src="https://user-images.githubusercontent.com/8583900/144759522-5306e61e-e30d-45e0-bb1a-ea8360e8c6da.png" width="70%" /></p>

5. Some tasks require the use of Paraview to view the 3D meshes produced.
Parview can be download from [here](https://www.paraview.org/download/).
    <details>
      <summary><b>Expand</b> - Ubuntu terminal commands for Paraview install</summary>
        <pre><code class="language-html">
        sudo apt update && sudo apt-get install paraview
        </code></pre>
    </details>

6. Some tasks require the use of CAD software to view the 3D geometry produced.
FreeCAD is one option for this and can be downloaded [here](https://www.freecadweb.org/downloads.php).
    <details>
        <summary><b>Expand</b> - Ubuntu terminal commands for FreeCAD install</summary>
            <pre><code class="language-html">
            sudo apt update && sudo apt-get install freecad
            </code></pre>
    </details>

# Run in the cloud

The repository is also ready for deployment on Github Codespaces which allows
users to launch the containerized environment on more powerful cloud computers
without installing anything locally.

- To get started sign up to codespaces :point_right: [codespaces](https://github.com/features/codespaces)

- Then follow :point_right: [this link](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=386229912) to config a compute instance :point_right: <p align="center"><a href="https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=386229912" target="_blank"><img src="https://user-images.githubusercontent.com/8583900/179179958-cc7f0700-6df5-47e9-a10f-67a9c1e556c6.png" height="150" /></a></p>

- VS Code will then launch in the browser, once loaded you must select the conda python interpreter to enable the correct Python environment.


# Workshop tasks

The task videos are all available on a [Gather Town](https://gather.town/app/QnHxhg6bPf8KQdii/openmc-workshop) space which is great for working through the workshop with colleagues.

| Tasks | Keywords | Video(s) |
|-|-|-|
| [Task 1 - Cross sections](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_01_cross_sections) | Nuclear data, cross-sections, MT numbers, Doppler | [link1](https://youtu.be/eBZ2lY_2v7I)  [link2](https://youtu.be/ELZNeIdSuMY) [link3](https://youtu.be/ec5BLLL6Q_g) [link4](https://youtu.be/mkl1mVnTO6g) |
| [Task 2 - Materials](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_02_making_materials) | Materials, Neutronics Material Maker, Mixed materials | [link](https://youtu.be/-NGnY-1TWCA) |
| [Task 3 - CSG geometry](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_03_making_CSG_geometry) | CSG geometry, Geometry visualisation | [link](https://youtu.be/Ovr7oYukYRw) |
| [Task 4 - Sources](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_04_make_sources) | Neutron point sources, Gamma sources, Plasma sources, Neutron track visualisation | [link](https://youtu.be/j9dT1Viqcu4) |
| [Task 5 - TBR](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_05_CSG_cell_tally_TBR) | Tritium Breeding Ratio, Cell tallies, Simulations | [link](https://youtu.be/Vc7Qy7QW4o8) |
| [Task 6 - DPA](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_06_CSG_cell_tally_DPA) | Displacements Per Atom, Cell tallies, Simulations, Volume calculations | [link](https://youtu.be/VLn59FSc4GA) |
| [Task 7 - Neutron and photon spectra](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_07_CSG_cell_tally_spectra) | Neutron Spectra, Photon Spectra, Cell tallies, Energy group structures, Flux, Current | [link](https://youtu.be/qHqAuqMLYPA) |
| [Task 8 - Mesh tallies](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_08_CSG_mesh_tally) | Mesh tallies, Structured meshes | [link](https://youtu.be/KYIsDjip1nQ) |
| [Task 9 - Dose](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_09_CSG_dose_tallies) | Instantaneous Dose, Cell tallies, Dose coefficients |  |
| [Task 10 - Making CAD geometry](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_10_making_CAD_geometry) | Parametric CAD geometry, Paramak, Geometry visualisation | [link](https://www.youtube.com/watch?v=Bn_TcJSOvaA) |
| [Task 11 - CAD Cell tallies](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_11_CAD_cell_tally_heat) | CAD-based neutronics, Cell tallies, DAGMC, Heating |  |
| [Task 12 - CAD Mesh tallies](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_12_CAD_mesh_fast_flux) | CAD-based neutronics, Mesh tallies, Paramak, DAGMC, Fast flux |  |
| [Task 13 - Variance_reduction](https://github.com/fusion-energy/neutronics-workshop/tree/develop/tasks/task_13_variance_reduction) | Variance reduction, weight windows |  |
| [Task 14 - Activation transmutation depletion](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_14_activation_transmutation_depletion) | Isotope build up and tally variation as a function of time |  |
| [Task 15 - Techniques for sampling parameter space](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_15_parameter_study_sampling) | Sampling, Interpolation, Multi-dimensional parameter studies |  |
| [Task 16 - Parameter study optimisation](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_16_parameter_study_optimisation) | Data science machine learning approaches |  |
| [Task 17 - Detector examples](https://github.com/fusion-energy/neutronics-workshop/tree/main/tasks/task_17_detector_examples) | Time filter detector response time of flight |  |
