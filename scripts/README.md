# kubeplugin

## Usage

```sh
./kubeplugin RESOURCE_TYPE NAMESPACE
```

for example:

```sh
./kubeplugin node default
```

You can also call it via kubectl:
```sh
kubectl kubeplugin node default
```

> You have to add scripts directory to the PATH for usage via kubectl
