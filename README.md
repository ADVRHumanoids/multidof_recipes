# multidof_recipes
Collection of forest recipes for multidof's software

# How to use
```
[sudo] pip3 install hhcm-forest
mkdir my_workspace && cd my_workspace
forest --init
source setup.bash
forest --add-recipes git@github.com:ADVRHumanoids/multidof_recipes.git master --update
forest <recipe-name> -j 4 
```

NOTE: to enable the *xeno flags*, you can use the command `forest -m xeno <recipe-name> -j 4`
