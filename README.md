# Tutorial Source Repository

This repository serves as a source to clone the files necessary for the tutorial. It includes the essential files and directory structure to follow along with the tutorial steps. However, please note the following important points:

## Missing Components

### 1. KUBECONFIG

The `KUBECONFIG` file, which is required for accessing your Kubernetes cluster, is not included in this repository. You will need to provide your own `KUBECONFIG` file to connect to your cluster.

### 2. Flux Bootstrap Manifests

Bootstrapping Flux creates various manifest files in the manifests folder, which are crucial for managing the state of your Kubernetes cluster with Flux. Although the manifests folder and its contents are already present in this repository, the bootstrapping of the cluster still needs to be performed by you to generate any additional necessary files and complete the setup.
With Flux installed, all the resources specified in the manifests folder will be created. You will only need to update the URLs in the **git-repository.yaml** and **image-repository.yaml**files.

### 3. Missing Secrets

To grant Flux access to your repository and your cluster, you need to create the ghcr-secret and git-secret secrets in your cluster. For detailed instructions, refer to the[Metal Stack Cloud Developer Guides](https://metalstack.cloud/en/documentation/DeveloperGuide/flux)

## 3. CI Configuration

This repository includes a sample `CI.yaml` file which you can use to run your own CI pipeline. This pipeline packages the `index.html` file as a Docker image and pushes it to GitHub Container Registry (GHCR), replacing the version with the current timestamp.

## Getting Started

To get started with this repository, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/x-cellent/FluxDeveloperguide.git
   cd Fluxdeveloperguide
   ```

2. **Add your KUBECONFIG file**:
   Copy your `KUBECONFIG` file to the appropriate location or set the environment variable:

   ```bash
   export KUBECONFIG=/path/to/your/kubeconfig
   ```

3. **Bootstrap Flux**:
   Follow the [Metal Stack Cloud Developer Guides](https://metalstack.cloud/en/documentation/DeveloperGuide/flux) to bootstrap Flux in your cluster. This will generate the necessary manifest files in the `manifests` folder:

## Additional Information

For comprehensive instructions on setting up and using Flux for automatic deployment, please refer to the official [Metal Stack Cloud Flux Deployment Guide](https://metalstack.cloud/en/documentation/DeveloperGuide/fluxdeployment).

For any issues or questions, feel free to open an issue in this repository.

Happy coding!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
