<div align="center"><img src="./docs/images/4844-logo-200px.png"/></div>
<h2 align="center">🐼 ❤️.oO<br>"Pandas love blobs"</h2>
<h1 align="center">Infrastructure code for EIP4844 Dev/Testnets</h1>

<p align="center">
<a href="https://github.com/ethpandaops/4844-testnet/actions/workflows/ansible_lint.yaml"><img src="https://github.com/ethpandaops/4844-testnet/actions/workflows/ansible_lint.yaml/badge.svg"></a>
<a href="https://github.com/ethpandaops/4844-testnet/actions/workflows/terraform_lint.yaml"><img src="https://github.com/ethpandaops/4844-testnet/actions/workflows/terraform_lint.yaml/badge.svg"></a>
<a href="https://github.com/ethpandaops/4844-testnet/actions/workflows/helm_lint.yaml"><img src="https://github.com/ethpandaops/4844-testnet/actions/workflows/helm_lint.yaml/badge.svg"></a>
</p>

This repository contains the infrastructure code used to setup [EIP4844](https://www.eip4844.com/) dev/testnets. A lot of the code uses reusable components either provided by our [ansible collection](https://github.com/ethpandaops/ansible-collection-general) or our [helm charts for kubernetes](https://github.com/ethpandaops/ethereum-helm-charts/).

# Networks

Status   | Network    | Links   | Ansible                                                      | Terraform | Kubernetes
------   | --------   | ----     |  -----                                                       | -------   | ------
 🔴 Off | [devnet-4](https://4844-devnet-4.ethpandaops.io/)   | [Network config](network-configs/devnet-4) / [Inventory](ansible/inventories/devnet-4/inventory.ini)     | [🔗](ansible/inventories/devnet-4) | [🔗](terraform/devnet-4) | [🔗](kubernetes/devnet-4)
 🟢 Live | [devnet-5](https://4844-devnet-5.ethpandaops.io/)  | [Network config](network-configs/devnet-5) / [Inventory](ansible/inventories/devnet-5/inventory.ini)     | [🔗](ansible/inventories/devnet-5) | [🔗](terraform/devnet-5) | [🔗](kubernetes/devnet-5)

# Development
## Version management for tools

We're using [asdf](https://github.com/asdf-vm/asdf) to make sure that we all use the same versions across tools. Our repositories should contain versions defined in .tools-versions.

You can then use [`./asdf-setup.sh`](./asdf-setup.sh) to install all dependencies.
