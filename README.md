# multidof_recipes
Collection of forest recipes for multidof's software

# How to use
```
pip3 install hhcm-forest
mkdir my_workspace && cd my_workspace
forest --init
source install/setup.bash
forest --add-recipes git@github.com:ADVRHumanoids/multidof_recipes.git master --update
forest all -j 4 
```
