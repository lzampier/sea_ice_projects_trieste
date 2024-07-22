# Tutorial for running basic Icepack installation at the School on Polar Climates (22/07/2024, Trieste, Italy) 

You are in luck! Icepack is an amazing modelling tool with fantastic documentation and support. Everything you want to know about the model is contained in the icepack documentation. This includes information on how to install, compile, and run the model, plus a lot of details on the physics implemented in it. The table of contents of the icepack documentation can be found [**HERE**](https://cice-consortium-icepack.readthedocs.io/en/main/index.html).

Some of the material I am using for introducing sea ice and Icepack in this first day of projects is taken from this fantastic presentation by Elizabeth Hunke and David Bailey. You can download the presentation from this [**Zenodo repository**](https://zenodo.org/records/11264197).

## STEP ONE – Configure Icepack Git repository

During this project, we will work with Git in different contexts. On this first day, Git will be used to download the code of Icepack, a state-of-the-art single-column sea ice model. However, you could also use GitHub to share the scripts you are working on, document your progress, and implement some testing. 

Therefore, it is important that you all have a running GitHub account and that you know its basic functionalities. You can follow this guideline provided by the CICE consortium, where explanations are provided on how to fork your version of the icepack repository. 

[**In this guide**](https://github.com/CICE-Consortium/About-Us/wiki/Git-Workflow-Guide), a lot of very important info is provided on how to interact with the main code of Icepack. Some of them are useful in the context of this project, but most of them go beyond the scope of this tutorial. I recommend reading them to familiarize yourself with the basic terminology, and to appreciate the complexity of running and maintaining a large geophysical model. The workflow guide is oriented toward setting up CICE rather than Icepack, but the same workflow applies to Icepack standalone.

At the end of step one, you should have your very own fork of the Icepack repository in your GitHub account.

## STEP TWO – Create a group repository to share the code you will produce during this project

Discuss and decide who could be a good manager for the git repository in your group. This person will create an empty repository to share with the rest of his group. You will decide if you want an open or closed repository, set the permission, decide on a branching strategy, etc. Each one of you should try to upload some code (a simple text is fine) so that the others can get it in their local repositories! 

## STEP THREE – Clone, setup, compile, and run Icepack

There is a [**detailed tutorial**](https://cice-consortium-icepack.readthedocs.io/en/main/appendices/tutorial.html) for a basic Icepack installation provided by the CICE Consortium. I recommend you follow that guide and try to have your first Icepack simulation running on your machine.

## STEP FOUR – NetCDF output in Icepack

Ok, very nice! You made it here. You run your first simulation with Icepack and you get some log output in the form of a text file (ugly)! We can do a bit better and get output in **NetCDF files**. 
If you have never worked with NetCDF, here is some information on the basic concept behind this data structure (copied from this [UCAR page](https://www.unidata.ucar.edu/software/netcdf/)). NetCDF (Network Common Data Form) is a set of software libraries and machine-independent data formats that support the creation, access, and sharing of array-oriented scientific data. It is also a community standard for sharing scientific data. The Unidata Program Center supports and maintains netCDF programming interfaces for C, C++, Java, and Fortran. Programming interfaces are also available for **Python**, IDL, MATLAB, R, Ruby, and Perl. Data in netCDF format is:

- **Self-Describing.** A netCDF file includes information about the data it contains.
- **Portable.** A netCDF file can be accessed by computers with different ways of storing integers, characters, and floating-point numbers.
- **Scalable.** Small subsets of large datasets in various formats may be accessed efficiently through netCDF interfaces, even from remote servers.
- **Appendable.** Data may be appended to a properly structured netCDF file without copying the dataset or redefining its structure.
- **Sharable.** One writer and multiple readers may simultaneously access the same netCDF file.
- **Archivable.** Access to all earlier forms of netCDF data will be supported by current and future versions of the software.

So, how do we get some netCDF output in Icepack? The basics can be found on [**this subsection of the documentation**](https://cice-consortium-icepack.readthedocs.io/en/main/user_guide/ug_implementation.html#history-files). Give it a go, and hopefully you will get some NetCDF output to look at in a few minutes.

## STEP FIVE – Different forcings for different problems. Running the model with ERA5.

TBC
