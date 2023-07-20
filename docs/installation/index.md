---
layout: default
title: Installation
nav_order: 3
---

# Instructions to install GoldSim

## Before installing
[GoldSim](https://www.goldsim.com/)  only works on Windows operating systems. Virtual machines are not generally recommended. GoldSim is a proprietary software and you will need a license to use it.

## License
For this workshop, we will have some student licenses available for this generously provided by GoldSim.

If you are a student (undergrad, master's or Ph.D.) go to the [GoldSim Academic Application Form for Students](https://www.goldsim.com/Forms/StudentAcademic/). Read the instructions carefully and fill out the form to get a licence. If you are a postdoc, professor or other category, fill out the [GoldSim Academic Application Form for Instructors](https://www.goldsim.com/Forms/InstructorAcademic/). After that, GoldSim experts will get back to you and provide you the basic information to finish installing the software. If your license expires or you need support with installation, contact the [GoldSim Customer Service](https://www.goldsim.com/Web/Customers/Support/).

## Installation instructions

1. Before downloading GoldSim, please ensure that your computer meets the [system requirements](https://media.goldsim.com/Documents/Software/RelNotes.htm) for the program.

2. You can download GoldSim [from the website](https://www.goldsim.com/Web/Customers/Downloads/GoldSim/Latest/).
![Install1](../figures/GoldSim_Install_1.png "Courtesy of GoldSim")
Image courtesy of GoldSim

3. Click on the download button
![Install2](../figures/GoldSim_Install_2.png "Courtesy of GoldSim")
Image courtesy of GoldSim

4. Once downloaded, run the .exe file.

5. During the installation process, you will be asked to input your activation id. This activation id will be provided to you during the workshop. If you have purchased GoldSim, or if you have requested an [academic](https://www.goldsim.com/Web/Purchase/AcademicResearch/#RequestAcademic) or [trial](https://www.goldsim.com/Forms/Trial/) license, you should have received an activation id.

### Installing GoldSim player
GoldSim player allows you to run certain files in GoldSim (player files). You cannot edit or change models, but it can be a useful option if you want to get an intuition of how GoldSim works.

1. To install GoldSim player files like the ones provided in the [repository](https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files), go to the [download page](https://www.goldsim.com/Web/Customers/Downloads/Player/)
![Install3](../figures/GoldSim_Player_Install_1.png "Courtesy of GoldSim")
Image courtesy of GoldSim

2. Click on the download button
![Install4](../figures/GoldSim_Player_Install_2.png "Courtesy of GoldSim")
Image courtesy of GoldSim


## After installation

I would strongly recommend to follow the [Introduction to GoldSim course](https://www.goldsim.com/Courses/BasicGoldSim/) and download the zip file with the exercises and examples. In my experience, you should at the very least complete the first four lessons before starting to work on your own projects. Ideally, you should complete the first nine lessons.

Open the GoldSim density-dependent model and play around with it. If you can’t find it, contact the GoldSim responsible person. What happens when you change the model's initial concentrations or growth rates? How does this model fit into your own project?

## Working on your own project: some tips

Before starting your own model in GoldSim, think about these questions:

1. What is your hypothesis for this model?
2. Do you need to do this? Has anyone done this before you? Ask or look at the literature.
3. What are the requirements (i.e., expected inputs and outputs)? Are they reasonable and realistic?
4. Before starting your model, sketch a diagram of what your model should do. [Cybernetic](https://en.wikipedia.org/wiki/Cybernetics) diagrams or tables can be useful.
5. Are the requirements still consistent with your cybernetic diagram or table? Modify them if they are not.
6. In most cases your model will need parameters or [data elements](https://help.goldsim.com/index.html#!Modules/5/inputelements.htm)  to work. Can you get their values from an experiment or the literature? 
7. What is a reasonable deadline to have the first version of the model, and what can you realistically do before that deadline? (remember that coding usually takes longer than expected)
8. Write an initial version of your model in paper (pseudo-code) 
9. Do a minimal version of the model that you can test.
10. Test that version and verify it works.
11. Start documenting your model and doing [version control](https://www.atlassian.com/git/tutorials/what-is-version-control#:~:text=Version%20control%2C%20also%20known%20as,to%20source%20code%20over%20time.). Use a [GitHub](https://github.com/) repository or other platform.
12. You never finish a model: you just do another iteration of it.


