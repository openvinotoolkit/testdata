# OpenVINO™ Toolkit Test Data Repository

This repository contains the data you need to pass all tests successfully.

## Tests That Require Using This Repository

* [`MklDnnFunctionalTests`](`inference-engine/tests_deprecated/functional/mkldnn`)
* [`MyriadFunctionalTests`](`inference-engine/tests_deprecated/functional/vpu`)
* [`InferenceEngineCAPITests`](`inference-engine/ie_bridges/c/tests`)
* [`InferenceEnginePythonAPITests`](`inference-engine/ie_bridges/python/tests`)

## Repository Components

* [Test models](./models/README.md) are required for low-precision transformations and the OpenVINO™
  toolkit Inference Engine bridges validation.
* [Image data](./validation_set) is required for low-precision transformations and the OpenVINO™
  toolkit Inference Engine bridges validation.
* [IE Class test XML-files](./ie_class) are required for the Inference Engine Core validation.
* [VPU test weights](./vpu) are required for some VPU layers validation.

## License

Deep Learning Deployment toolkit is licensed under the [Apache License Version 2.0](LICENSES/Apache_2.0_LICENSE). By
contributing to the project, you agree to the license and copyright terms therein and release your
contribution under these terms.

## Usage

Choose one of the ways to download this repository and follow the steps to start using the tests:

* **Download the repository automatically**  
    1. Add the additional CMake `-DENABLE_DATA=ON` option when building the project. Use the
       `-DENABLE_FUNCTIONAL_TESTS=ON` option to download the repository automatically to the
       `inference-engine\temp\data\src\data` directory.
    2.  Go to the `inference-engine\temp\models\src\data` directory, open a terminal, and enter the
        command to download the large file storage:
    ```bash
    git lfs pull
    ```
    3. Run tests

* **Clone the repository manually**  
    1. Open a terminal and clone the repository:
    ```bash
    git clone https://github.com/openvinotoolkit/testdata.git
    ```
    2. In the same terminal, go to the repository directory:
    ```bash
    cd testdata
    ```
    3. Download the large file storage:
    ```bash
    git lfs pull
    ```
    4. Set environment variables. Replace `{PATH_TO_REPOSITORY}` with the directory you cloned the
       repository to:
    ```bash
    DATA_PATH={PATH_TO_REPOSITORY}/testdata
    ```
    ```bash
    MODELS_PATH={PATH_TO_REPOSITORY}/testdata
    ```
    5. Run tests

## How to Contribute

Your contributions are welcome. Follow these steps:

1. Make sure you can build the product and run all tests and samples with your patch.
2. Add the license to `third-party-programs.txt`. If the license is not 
yet in the repository, add a file with it as well.
3. [Submit a pull request](https://github.com/openvinotoolkit/testdata/pulls) and
explain its purpose in the description.

We assign your pull request to the maintainers. Once you obtain an approval, you can add new test data. 
The maintainers review your contribution, request additional fixes or modifications 
if necessary, and merge the pull request into the GitHub* repository.

## Support

To report questions, issues, and suggestions use [GitHub
Issues](https://github.com/openvinotoolkit/openvino/issues).

