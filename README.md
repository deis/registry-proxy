
|![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/Warning.svg/156px-Warning.svg.png) | Deis Workflow will soon no longer be maintained.<br />Please [read the announcement](https://deis.com/blog/2017/deis-workflow-final-release/) for more detail. |
|---:|---|
| 09/07/2017 | Deis Workflow [v2.18][] final release before entering maintenance mode |
| 03/01/2018 | End of Workflow maintenance: critical patches no longer merged |

# Deis Registry Proxy

Deis (pronounced DAY-iss) Workflow is an open source Platform as a Service (PaaS) that adds a developer-friendly layer to any [Kubernetes](http://kubernetes.io) cluster, making it easy to deploy and manage applications on your own servers.

For more information about the Deis Workflow, please visit the main project page at https://github.com/deis/workflow.

We welcome your input! If you have feedback, please [submit an issue][issues]. If you'd like to participate in development, please read the "Development" section below and [submit a pull request][prs].

# About

registry-proxy is a proxy deployed on every Kubernetes worker node, proxying all requests to the Deis Workflow [registry][registry]. This allows the worker nodes' Docker daemons to communicate to the registry over localhost, bypassing the need for adding the `--insecure-registry` flag to the daemons.

# Development

The Deis project welcomes contributions from all developers. The high level process for development matches many other open source projects. See below for an outline.

* Fork this repository
* Make your changes
* [Submit a pull request][prs] (PR) to this repository with your changes, and unit tests whenever possible.
  * If your PR fixes any [issues][issues], make sure you write `fixes #1234` in your PR description (where #1234 is the number of the issue you're closing)
* The Deis core contributors will review your code. After each of them sign off on your code, they'll label your PR with LGTM1 and LGTM2 (respectively). Once that happens, the contributors will merge it

## Testing Your Code

When you've built your new feature or fixed a bug, make sure you've added appropriate unit tests and run `make test` to ensure your code works properly.


[issues]: https://github.com/deis/registry-proxy/issues
[prs]: https://github.com/deis/registry-proxy/pulls
[registry]: https://github.com/deis/registry
[v2.18]: https://github.com/deis/workflow/releases/tag/v2.18.0
