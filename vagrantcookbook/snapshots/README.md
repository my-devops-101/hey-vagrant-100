# Snapshots

> Since version 1.8, Vagrant comes with the ability to take snapshots of VMs.


```bash
vagrant snapshot push
```

```bash
vagrant snapshot pop
```


## Working with Multiple Snapshots

```bash
vagrant snapshot save base-env
```

```bash
vagrant snapshot restore base-env
vagrant snapshot delete base-env
```

```bash
vagrant snapshot list
```

