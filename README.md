# Kosarev Space Deployment GitHub Action

This GitHub Action triggers a deployment on Kosarev Space.

## Inputs

### `auth_token`

**Required** Kosarev Space authentication token.

### `service_id`

**Required** Kosarev Space service ID.

## Usage

To use this action, include it in your workflow file as follows:

```yaml
name: Deployment Workflow

on: [push]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout
      uses: actions/checkout@v4

    - name: Deployment
      uses: kosarev-space/deploy-action@0.0.1
      with:
        auth_token: ${{ secrets.KOSAREV_SPACE_AUTH_TOKEN }}
        service_id: ${{ secrets.KOSAREV_SPACE_SERVICE_ID }}
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or feature requests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
