These mkfiles can be used as is or as basis for your own mkfiles. Unlike standard files in `/mkfiles` these know how to handle `/opt` packages; able to build/run tests (both in host os and inside emu) and have other features (generation of INDEX files for your man pages, generation of man pages from text in asciidoc markup, etc.).

Start your new project using these mkfiles:

```
$ emu
; mkdir newproject
; cd newproject
; cp /opt/mkfiles/mkconfig-example mkconfig
; cp /opt/mkfiles/mkfile-example mkfile
```

See example project skeleton/template: http://code.google.com/p/inferno-opt-skel/


---


To install system-wide (if your Inferno installed in your home directory or if you root):

```
hg clone https://code.google.com/p/inferno-opt-mkfiles/ $INFERNO_ROOT/opt/mkfiles
```

To install locally for some project:

```
$ cd YOUR_PROJECT_DIR
$ mkdir -p opt/
$ hg clone https://code.google.com/p/inferno-opt-mkfiles/ opt/mkfiles
$ emu
; cd YOUR_PROJECT_DIR_INSIDE_EMU
; bind opt /opt
```