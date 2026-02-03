# MLopsStudy2

### Initialize DVC repository
```sh
dvc init
```

### add the file to the repository
esto crea un archivo con el mismo nombre y extensión `.dvc` y tambien crea el archivo `.gitignore` dentro de data con el ignore al archivo .csv

```sh
dvc add data/wine_sample.csv
```

el archivo vsc pesado no se sube a git, solo se sube el dvc con el checksum que hace referencia al archivo pesado

### DVC remote

```sh
dvc remote add -d wine_remote s3://clean-zone-sca/dvc/
dvc push
```