# Setup

## Before running ansible
* For Linux:
  - If you want to test changes with the docker workbench image, you need docker installed.
* For macOS:
  - Test changes with a [UTM](https://mac.getutm.app/) virtual machine.
  - Install Xcode command line tools to get python and git
  - Install Homebrew
* Install ansible
  - Install using homebrew on mac
  - Install using pip on Linux
* Set up ssh
* Download this repo

## Run ansible from within the OS folder
`ansible-playbook local.yml -K --tags <tags>`

