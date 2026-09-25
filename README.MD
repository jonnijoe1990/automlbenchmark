usage:

```
from automlbenchmark import run

constraints = ["30m", "1h"]
frameworks = ["AutoGluon", "flaml", "H2OAutoML"]
task = "gender"
folds = 5


for c in constraints:
    for fold_num in range(folds):
        for f in frameworks:
            run([f, "sap", c, "-t", task, "-m", "docker", "-f", fold_num])

```
