# Helm Charts

This repository contains Helm charts for various applications by @dejanualex

## Usage

Add this Helm repository:

```bash
helm repo add dejanu https://dejanu.github.io/chartsrepo/
helm repo update
helm search repo dejanu
helm install my-release dejanu/sample-app
```

## Development

To add a new chart:

1. Create the chart in the `charts/` directory:
   ```bash
   helm create charts/my-new-chart
   ```

2. Package the chart:
   ```bash
   helm package charts/my-new-chart
   ```

3. Update the repository index:
   ```bash
   helm repo index . --url https://dejanu.github.io/chartsrepo/
   ```

4. Commit and push the changes to trigger GitHub Pages deployment.

## Repository Structure

```
.
├── charts/          # Source charts
├── *.tgz            # Packaged charts
├── index.yaml       # Repository index
└── README.md        # This file
```
