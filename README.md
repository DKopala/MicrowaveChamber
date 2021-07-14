# MicrowaveChamber

Case on microwave modelling presented on Elmer webinar series - 20th of May, 2021.

**"Industrial applications oriented, microwave modelling in ELMER"**

Presentation available [here](https://www.nic.funet.fi/pub/sci/physics/elmer/webinar/)

## File data

First published: **19th of May, 2021**

File list:
- GEO. file: geometry model - run by Netgen software
- SIF. file: solver intput file - run by ELMER FEM software

## Description

Project of the microwave chamber with a waveguide. It allowed study on the resonance phenomenon in microwave chamber modelled with MES software.

## 3D model - Netgen

Device consists of two parts: cylindrical waveguide and cylindrical chamber. They are joined axisymmetricly.

>![Model 3D - geometry](/img/Org_3D_geo.png)

## Model's mathematical description - Elmer FEM

Model's interior is filled with air - its parameters are approximated with parameters of vacuum in *Material* section.

`Relative Permittivity = Real 1`

Model uses *VectorHelmholtz* module for solving Helmholtz equation describing electromagnetic wave propagation. It is provided in *Solver 1* section. Moreover *Solver 2* provides solver, which allows calculating results from *VectorHelmholtz* module. *Solver 3* allows saving results describing chamber's area in YZ plane to an external data file.

Model is described with two boundary conditions.

>![Model's boundary conditions](/img/ORG_b_conditions.png)

### Inport

Inport is a source of electromagnetic wave. It is described with specific Helmholtz equation for the case:


### Walls

Energy absorption by copper walls are described with Leontovich impedance boundary condition.

## Usage

Project was implemented for educational purposes.

## Gallery

Visualisation of the electromagnetic field distribution inside a model given in YZ plane.

> ### Electric field E
>
>
> ![Electric field vector distribution, imaginary part](/img/ORG_E_field_im_YZ.png)

> ### Magnetic field strength H
>
> ![Magnetic field strength distribution, real part](/img/ORG_M_field_re_YZ.png)
>
> ![Magnetic field strength distribution, imaginary part](/img/ORG_M_field_im_YZ.png)
