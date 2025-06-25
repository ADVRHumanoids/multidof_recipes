# multidof_recipes
Collection of forest recipes for multidof's software 

# How to use
```
[sudo] pip3 install hhcm-forest
mkdir my_workspace && cd my_workspace
forest init
source setup.bash
forest add-recipes git@github.com:ADVRHumanoids/multidof_recipes.git --tag master
forest grow <recipe-name> -j 4 
```
