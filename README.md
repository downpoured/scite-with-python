# SciTE-with-Python

A fork of the SciTE code editor that adds Python extensiblity. In addition to standard multi-tab code editing, this project lets you create plugins to help you write code more efficiently.
    
* plugins can use the Python standard library, for example,

    * sorting the selected lines of text
    
    * restyling ranges of text to underline or highlight
    
    * automating nearly every editor action
    
    * showing an interactive GUI inside the code editor
    
    * shelling out to other tools with Python's subprocess
    
* plugins can register for events like OnKey, OnOpen, and OnSave, for example,

    * letting you listen for multi-key keyboard shortcuts
    
    * auto-completing xml tags, or writing snippets a la TextMate
    
    * showing file metadata when files are opened

* additions to SciTE include

    * use "menukey" to customize keyboard bindings
    
    * find-text-in-files now has regular expression support

    * when multiple editor windows are open, the search state is shared
    
    * 26 plugins for manipulating text, finding filenames, and navigating to declaration/definition of the selection in C source code
    
## Documentation

[usage and features](https://downpoured.github.io/scite-with-python/070/usage_and_features.html)

[writing plugins](https://downpoured.github.io/scite-with-python/070/writing_plugins.html)

[compiling for Windows](https://downpoured.github.io/scite-with-python/070/compile_for_windows.html)

## Windows

* install [Python 2.7](https://www.python.org/downloads/windows/), select Windows x86 MSI installer

* download scite-with-python.zip from [scite-with-python](https://github.com/downpoured/scite-with-python) and uncompress 

* open SciTE.exe

## Linux

    # install prereqs
    sudo apt-get install libgtk2.0-dev
    sudo apt-get install python2.7-dev

    # build scintilla and scite
    mkdir ~/scite-with-python
    cd ~/scite-with-python
    git clone https://github.com/downpoured/scite-with-python.git
    cd scite-with-python/src/scite/scintilla/gtk
    make
    cd ../../scite/gtk
    make
    sudo make install

    # run scite
    /usr/bin/SciTE_with_python
