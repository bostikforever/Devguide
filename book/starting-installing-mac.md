# Installing Files and Code

Usage of the [Homebrew package manager](http://mxcl.github.com/homebrew/) for Mac OS X is recommended. The installation of Homebrew is quick and easy: [installation instructions](http://mxcl.github.com/homebrew/).

After installing Homebrew, copy these commands to your shell:

<div class="host-code"></div>

```sh
brew tap PX4/homebrew-px4
brew update
brew install genromfs
brew install kconfig-frontends
brew install gcc-arm-none-eabi
brew install astyle
brew install cmake
```

Then install the required python packages:

<div class="host-code"></div>

```sh
sudo easy_install pip
sudo pip install pyserial empy
```

Now continue to run the [first build](starting-building.md)!
