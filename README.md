# bd-brewfile

The `Brewfile` in this repository was generated from NC State University Libraries' born-digital processing workstation. We use Homebrew to manage the majority of the applications we use in our work. This file can be used on Mac OS and Linux to quickly install a set of packages we find useful for digital archival extracting and reporting procedures.

More information about how we use some of the tools listed in the Brewfile can be found in [BitCurator: Beyond Environment](https://bitcuratorconsortium.org/bitcurator-beyond-environment-2/). 

## Install packages from a Brewfile

Assuming [Homebrew](https://brew.sh/) is installed on your computer, download the Brewfile from this repository and type in a terminal:

`brew bundle --file=/path/to/Brewfile`

updating "/path/to/file" to where you have the Brewfile saved locally.

This Brewfile is likely to change over time.

### Please note!

If you are already using Homebrew to manage things, installing packages in reference to this Brewfile _should_ add to what you already have installed. However, for the sake of safety, please first make a back-up by creating your own Brewfile by typing in a terminal:

`brew bundle dump`

The Brewfile should be written to the home directory of the user account you're currently logged in as. 

## Helpful background

The article [macOS migrations with Brewfile](https://openfolder.sh/macos-migrations-with-brewfile) provides a useful overview of the `bundle` Homebrew package, used in generating and installing packages through referencing Brewfiles. It also goes into some detail about Homebrew, more generally. 

We haven't tesetd Homebrew on Linux, but there is [documentation available](https://docs.brew.sh/Homebrew-on-Linux) on the Homebrew site.

## Other applications NOT in the Brewfile

The following assumes you have already run the `brew bundle` installation command.

### Brunnhilde

We use (and love) Tessa Walsh's [Brunnhilde](https://github.com/tw4l/brunnhilde), but, unfortunately, it's not available through Homebrew. If you have `pip` set up, you can run

`sudo pip install brunnhilde`

_Most_ dependencies will be installed via the Brewfile, so do that before installing Brunnhilde. Note you'll also need to install hfsexplorer. See Tessa's instructions for that. 

#### pip
On the subject of pip, you can also manage packages with pip. See [12.3. Managing Packages with pip](https://docs.python.org/3/tutorial/venv.html#managing-packages-with-pip).

### ClamAV set up

While clamav IS available as a Homebrew package, you'll need to do some additional work to get it running. This has worked for us (clamav will be installed via the Brewfile, so you can skip `brew install clamav`):

[Get ClamAV running on Mac OS X (using Homebrew)](https://gist.github.com/subharanjanm/be799ee57854109c3860dde9ad823754)

## Acknowledgments

I'd like to thank my late friend and colleague Bret Davidson for first suggesting Brewfile as a lightweight approach to sharing one's processing environment. I'd also like to thank Robert Manly of Washington University in St. Louis for his willingness to test this out, and for his insightful feedback and suggestions that have made their way into this README.

## Author/Maintainer

- Brian Dietz (bjdietz at ncsu dot edu)

## License

See MIT-LICENSE