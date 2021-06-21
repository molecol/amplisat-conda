# The way to install conda on our servers (it must be improved)

1. Creation of new conda environment based on the recipe:

```
conda create --name <env_name> --file conda_recipe.txt
```

*Note that there are too many packages than required e.g. perl or cpan. It should be possible to use some of globally installed versions.*

2. Environment activation

```
conda activate <env_name>
```

3. Local installation of perl modules:

```
cpan -I -i File::FindLib
cpan -I -i Text::Iconv
```

*-I argument forces local installation*
*I am aware that you can somehow install perl modules within conda using cpanm but I don't really know how to include it later on in the single conda recipe.*

4. Copying AMPLISAT files stored at Leskowiec (path below):

```
usr/bin/amplisat
```
