# Charts
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Helm Charts repository for decyjphr-org.
## Usage

[Helm](https://helm.sh/) must be installed to use the charts. Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:

```bash
$ helm repo add decyjphr https://decyjphr-org.github.io/charts/
$ helm install ghas-compliance decyjphr/ghas-compliance
```

You can then run `helm search repo ghas-compliance` to see the charts.

You can then run `helm show values decyjphr/ghas-compliance` to see the values.

Chart documentation is available in [decyjphr directory](https://github.com/decyjphr-org/ghas-compliance/).

Install template with values for APP_ID, PRIVATE_KEY, WEBHOOK_SECRET using `--values` (Preferred approach)
```bash
helm install ghas-compliance decyjphr/ghas-compliance --values myvalues.yaml
```

Install template with values for APP_ID, PRIVATE_KEY, WEBHOOK_SECRET using `--set`
```bash
helm install ghas-compliance decyjphr/ghas-compliance --set appEnv.APP_ID="\"210920\"" --set appEnv.PRIVATE_KEY="TFM...==" --set appEnv.WEBHOOK_SECRET="ZjZlYTFjN...=="
```

Generate Kubernetes YAMLs
```bash
helm template ghas-compliance decyjphr/ghas-compliance --values myvalues.yaml
```

## Contributing

We'd love to have you contribute! Please refer to our [contribution guidelines](https://github.com/decyjphr-org/charts/blob/main/CONTRIBUTING.md) for details.

## License

[Apache 2.0 License](https://github.com/decyjphr-org/charts/blob/main/LICENSE).