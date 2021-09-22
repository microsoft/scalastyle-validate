# Scalastyle Validate Action [![Build](https://github.com/microsoft/scalastyle-validate/actions/workflows/ci.yml/badge.svg)](https://github.com/microsoft/scalastyle-validate/actions/workflows/ci.yml)

GitHub Action that examines your Scala code and indicates potential problems with [Scalastyle](http://www.scalastyle.org/).

## When to use

This action is useful when you need to examine your Scala code to idetify potential style problems and thow an error if a warning was found.

## How it works

1. The GitHub Action first eximines the Scala code in a given path.
2. The GitHub Actions checks if a warning was found. If no warning was found, then it suceeds, else it would throw an error.

## Getting Started

### Prerequisites

* Make sure you have a [Scalastyle configuration file](http://www.scalastyle.org/configuration.html) (scalastyle_config.xml) with your defined rules.
* Make sure you have setup Java
* Make sure you have setup Scala
* Make sure you have downloaded Scalastyle. A suggested GitHub Action to perform this can found [here](https://github.com/marketplace/actions/scalastyle-download).

A sample GitHub Action Workflow that shows the prerequisites can be found in this repository.

### Usage

```yml
steps:
    - name: Validate Scala Code
      uses: microsoft/scalastyle-validate@v1.0.0
      with:
        scala-code-directory: './path-to-code'
        scalastye-config-directory: './path-to-configfile'
        scalastyle-directory: './path-to-scalastyle'
```

### Inputs

| Name | Description | Required | Default value |
| --- | --- | --- | --- |
| `scala-code-directory` | Path to the Scala code | true | NA |
| `scalastye-config-directory` | Path to the Scalastyle configuration file | true | NA |
| `scalastyle-directory` | Path where the Scalastyle jar is downloaded. Default value assumes is in the same working directory | false | scalastyle.jar |


## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
