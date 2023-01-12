# DVC submodule for MLOPS Practice

Here a tutorial from DVC is shown.
Generally, to initialize a DVC project you must run the following at your project root (consider that `dvc` is a global
dependency and python >=3.8 is required.)

```bash
pip install dvc

cd dvc-project/
git init
dvc init
git commit -m "Init DVC"
```

1. Install requirements

    ```bash
    pip install -r src/requirements.txt
    ```

2. Get data from remote storage.

    ```bash
    dvc pull
    ```
   Remote storages are listed in `.dvc/config` and you can see them hitting the following:
    ```bash
    dvc remote list
    ```
   Remote storages allow to save our work, models, experiments and data to reproduce them.

3. To reproduce the pipeline, run the following
   ```bash
   dvc repro
   ```