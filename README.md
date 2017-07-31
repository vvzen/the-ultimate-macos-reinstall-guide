# MURG: MacOS Ultimate Reinstall Guide

#### Latest update: 31/07/2017

My ultimate list for ***Don't Panic!*** when I've got to reinstall everything from scratch on a new mac or after a format.

This is slowly becoming also my guide to setup a clean working environment when switching among different studios.
For this reason an experimental branch now exists covering additional tools required for pipeline development under windows. 

For a longer reading with explanations about each package, I suggest you to visit this awesome guide by Sourabh Bajaj: [http://sourabhbajaj.com/mac-setup/](http://sourabhbajaj.com/mac-setup/) .

=====


## Package managers:

One good idea would be to **always have a list of all packages currently installed** on your system so that whenever you'll be doing a clean reinstall you know exactly which packages you need.

Using homebrew, this can be as simple as that:

```brew leaves > brew_installed_packages.txt```

For cask apps:

```brew cask list > brew_cask_installed_packages.txt```


1. ### homebrew

	The missing macOS packager!

	![homebrew-icon](./images/homebrew-100.png)

	[http://brew.sh/index_it.html](http://brew.sh/index_it.html)

	```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
	
	Get info on package: ```brew info packagename```<br>
	Search pkgs: ```brew search packagename``` <br>
	Install pkgs: ```brew install packagename``` <br>
	Show installed pkgs: ```brew list``` <br>

2. ### homebrew cask

	For installing apps view brew.
	
	[https://caskroom.github.io](https://caskroom.github.io)

	```brew tap caskroom/cask```
	
## Command line tools:

1. ### wget

	```brew install wget```
	
2. ### git

	source control!
	
	```brew install git```
	
3. ### XCode command line tools

	1. check if xcode is installed:
		```xcode-select -p```	
	2. then
		```xcode-select --install```
	3. check if installation went good:
		```gcc --version```

## Shell:

1. ### oh-my-zsh

	![oh-my-zsh-icon](./images/oh-my-zsh-200.png)

	[https://github.com/robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
	
	**via curl:**
	
	```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
	
	**via wget:**
	
	```sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"```
	
	Theme: ```ZSH_THEME="zhann"```
	
	Font: `Menlo 11 pt.`

## Text editor

1.	![atom-icon](./images/atom.png)

	The open source hackable text editor for the 21st Century
	
	```brew cask install atom```
	
2. ### Visual Studio Code

	![asd](./images/visual-studio-code-200.png)
	
	The open source text editor from windows, with great performance
	
	```brew cask install visual-studio-code```
	
	**Extensions**:
	
	1. ```ext install beautify```
	2. ```ext install Dracula Theme```
	3. ```ext install Handlebars```
	4. ```ext install HTML Snippets```
	5. ```ext install Material-theme```
	6. ```ext install TODO Highlight```
	7. ```ext install Markdown Preview Enhanced```
	8. ```ext install vscode-icons```
	
3. ### Macdown
	
	![macdown](images/macdown-100.png)
	
	```brew cask install macdown```
	
## Javascript Dev:


1. ### Nodejs

	![nodejs-icon](./images/nodejs-128.png)
		
	1. ```brew install node``` will install both node and npm
	
	2. check that node and npm are correctly installed:
	
		```node -v```
	
		```npm -v```
2. ### NodeJS version manager

	For easing switching between node versions, LTS, etc..
	
	[https://github.com/tj/n](https://github.com/tj/n)
	
	```npm install -g n```
3. ### Gulp
	Instally globally:
	
	```npm install -g gulp```
	
	and locally to the project:
	
	```npm install --save-dev gulp```
	
# Python

1. ```brew install python3```
	
	Along with Python 3, Homebrew will install pip, setuptools and wheel.

2. Additional packages:
	
	see also: [installing-keras-for-deep-learning](http://www.pyimagesearch.com/2016/07/18/installing-keras-for-deep-learning/)
	
	1. **Numpy** ```pip3 install numpy```
	
	
# Utility

1. ### Dash

	![dash-icon](./images/dash-64.png)
	
	Get offline access to 150+ API documentation sets.
	
	[https://kapeli.com/dash](https://kapeli.com/dash)
	
2. ### Imagemagick

	![image-magick-icon](./images/wizard-128.png)
	
	The all in 1 image manipulation software run from command line.
	
	```brew install imagemagick```
	
	A simple example of resizing an image:
	
	```convert input.jpg -resize 50% output.jpg```

3. ### Handbrake 	
	![handbrake-icon](./images/handbrake-100.png)
		
	Tool for converting video from nearly any format to a selection of modern, widely supported codecs.
	
	```brew install handbrake```
	
	simple conversion example:
	
	```handbrakeCLI -i input.mov -o output.mp4```
	
	a more complex one (x264 codec, quality 20, audio as 160kbps AAC):
	
	```handBrakeCLI -i VIDEO_TS -o movie.mp4 -e x264 -q 20 -B 160```
	
	
4. ### Color Maker
	
	A nice color picker app with hex output.
	
	[https://itunes.apple.com/it/app/color-maker/id561995913?mt=12](https://itunes.apple.com/it/app/color-maker/id561995913?mt=12)
	
3. ### Crontab-UI

	A nice interface for managing cron jobs with crontab.
	
	[https://github.com/alseambusher/crontab-ui](https://github.com/alseambusher/crontab-ui)
		
	```npm install -g crontab-ui``` then to open it ```crontab-ui```
	
## Gimmicks
1. ### Quick look plugins

	See [this repo](https://github.com/sindresorhus/quick-look-plugins) for more infos!
	
	Preview source code files with syntax highlighting
	
	```brew cask install qlcolorcode```
	
	Preview JSON files
	
	```brew cask install quicklook-json```
	
	Display image size and resolution
	
	```brew cask install qlimagesize```


## Science&Math

1. ### Octave 

	![octave-icon](./images/octave-64.png)
	
	First ```brew tap homebrew/science``` then you can ```brew install octave```
	
	
## Data Science

1. ### R 
	![img](images/R-logo-100.png)
	
	After tapping science you can
	
	```brew install Caskroom/cask/xquartz```
	
	```brew install r```
	
	If you've got ```libgfortran.3.dylib: image not found``` error when opening RStudio from Finder/Spotlight, check this [github issue](https://github.com/Homebrew/homebrew-science/issues/2286).
	
2. #### Converters
	
	1. **Csv to GeoJSON**
		
		See [https://github.com/mapbox/csv2geojson](https://github.com/mapbox/csv2geojson)
		
	2. **Shape file to GeoJSON**
		
		Install [GDAL](http://www.gdal.org) : ```brew install gdal``` 
		
		Then you can:
		
		```ogr2ogr -f GeoJSON output.json -t_srs crs:84 input.shp```
		
		(using *crs:84* as projection)
	
	3. **GeoJSON to TopoJSON**
		
		This script requires the installation of **Node** and **Npm**.
		
		```npm install -g topojson```
		
		```geo2topo -i input.json -o output.json``` 
		
		See [here](https://github.com/topojson/topojson-server/blob/master/README.md) for more info.
		 

## Glitch art

1. ### Avidemux
	
	Video editor for datamoshing!
	
	```brew cask install avidemux```
	
2. ### byebyte

	![img](images/byebyte.png)

	*destroy your files in the name of art*
	
	[github repo](https://github.com/wayspurrchen/byebyte)
	
	```npm install -g byebyte```
