# OHIF stress/fuzz test

Simulate heavy usage of the Open Health Imaging Foundation (OHIF) zero-footprint medical image viewer.

Date: 12/19/2023

Fulmine Labs LLC

## Overview

The problem: The current automated tests of the excellent, open source, OHIF Basic Viewer are mainly functional in nature [(unit and end-to-end)](https://docs.ohif.org/development/testing).
In order to fush out any issues and increase confidence in the stability of this interface, it would be good to extend the available automated tests to also cover non-functional scenarios, such as performance. 

This Python/Selenium code, run from Jupyter notebook or Jupyter lab, performs a set of pseudo-randomized (fuzz) actions on the OHIF Basic Viewer across a number of studies. The code has the capabilty of graphing resource usage.
The number of iterations of the actions on each study and the number of studies can be tuned such that the script simulates heavy, but somewhat realistic usage of this interface over a period of time that simulates a long usage session (for example 8+ hours). 
The test logs resource usage during these iterations, which can be graphed after test completion.
In order for the test actions to run quickly and minimize user interface dependencies, which can be a notorious issue with UI based tests, there are no explicit verifications during the test. Therefore a passed test consists of: 
1) Completion of all iterations without encountering stability issues in the interface. This can be confirmed after a completed run by checking the test logs for unexpected conditions.
2) Non-increasing resource usage, after the initial startup.

## Current Version
The current stable version of the project is 0.1.0 See the [CHANGELOG.md](./CHANGELOG.md) for details about this release.

## Prerequisites




## Usage

1) Install Anaconda
2) Clone the OHIF-stress-fuzz-test repository to your local machine and navigate to the cloned directory in Anaconda Powershell Prompt: 'cd LNRoutingVizualization'
3) Install the dependencies listed in requirements.txt with `'pip install -r requirements.txt'`
5) Open Jupyter Notebook or Jupyter Lab from Anaconda
6) Open _.ipynb_ from the cloned directory inside Jupyter
7) Edit any display parameters in the first cell, as needed
8) In Jupyter 'Run All Cells'. 

## Screenshots/Recordings

If successful the running test should look something like this:

[![Video](https://www.dropbox.com/scl/fi/ko5j0ughrvm6aoa3yvywp/stress_test_1.png?rlkey=mohp2tt6kz863y14cluyjwfrl&raw=1)](https://www.dropbox.com/scl/fi/0oiqerzekj1otofjvqclj/stress_test_1.mp4?rlkey=lk0wyengm15pd5okdyhqmqopa&raw=1)

## Testing

This code was run in Jupyter Notebook and Jupyter Lab from Anaconda 2.5.1 on Windows 11.
OHIF Worklist, Basic Viewer from https://viewer.ohif.org/, version 3.7.0.

## Known issues

## Acknowledgements

* This code was written collaboratively with GPT-4V. Thank you Assistant!
* The Open Health Imaging Foundation

## License

[MIT open source license](LICENSE.txt)

## Collaboration

We welcome contributions at all levels of experience, whether it's with code, documentation, tests, bug reports, feature requests, or other forms of feedback. If you're interested in helping improve this tool, here are some ways you can contribute:

- **Ideas for Improvements**: Have an idea that could make the OHIF Stress Fuzz test better? Open an issue with the tag `enhancement` to start a discussion about your idea.
- **Bug Reports**: Notice something amiss? Submit a bug report under issues, and be sure to include as much detail as possible to help us understand the problem.
- **Feature Requests**: If you have a suggestion for a new feature, describe it in an issue with the tag `feature request`.
- **Documentation**: Good documentation is just as important as good code. Although this is currently a very simple tool, if you'd like to contribute documentation, we'd greatly appreciate it.
- **Code**: If you're looking to update or write new code, check out the open issues and look for ones tagged with `good first issue` or `help wanted`.

## Contact

Duncan Henderson, Fulmine Labs LLC
henderson.duncanj@gmail.com

