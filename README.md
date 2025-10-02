# Oracle Cloud CLI Sample Commands

A list of sample commands for the Oracle Cloud CLI.

> Git repo: https://github.com/farisdurrani/oci-cli-sample-commands <br/>
> Author: Faris Durrani <br/>

## Sample Commands

1. Get tenancy ID

```sh
oci iam compartment list --query 'data[?contains("compartment-id", `.tenancy`)]."compartment-id" | [0]' --raw-output
```

2. Get home region

```sh
oci iam region-subscription list --tenancy-id <tenancy-id> --query 'data[?"is-home-region"==`true`] | [0] | "region-name"' --raw-output
```

3. List all compartments

```sh
oci iam compartment list --compartment-id-in-subtree true --all
```

## License

See [LICENSE](LICENSE).
