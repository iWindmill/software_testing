Лог неудачной попытки настроить среду для автотестов. С PyCharm, Python и macOS в очередной раз стало ясно, что любая инструкция в сети не является гарантом успешности. Лог на всякий случай, если буду повторно пытаться взять высоту.

## День первый

14:19. Открыть публикацию "[Step by Step Selenium With Python – Part 1](http://scrolltest.com/2016/12/12/step-step-selenium-python-part-1/)". Публикация не пугает своей длиной, предназначена для пользователей macOS и содержит инструкции для командной строки.

14:21. Установить пакетный менеджер для Python командой
```
sudo easy_install pip
```

Получил не один warning:

```
Running pip-9.0.1/setup.py -q bdist_egg --dist-dir /tmp/easy_install-fOMral/pip-9.0.1/egg-dist-tmp-DPYdKF
/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/distutils/dist.py:267: UserWarning: Unknown distribution option: 'python_requires'
  warnings.warn(msg)
warning: no previously-included files found matching '.coveragerc'
warning: no previously-included files found matching '.mailmap'
warning: no previously-included files found matching '.travis.yml'
warning: no previously-included files found matching '.landscape.yml'
warning: no previously-included files found matching 'pip/_vendor/Makefile'
warning: no previously-included files found matching 'tox.ini'
warning: no previously-included files found matching 'dev-requirements.txt'
warning: no previously-included files found matching 'appveyor.yml'
no previously-included directories found matching '.github'
no previously-included directories found matching '.travis'
no previously-included directories found matching 'docs/_build'
no previously-included directories found matching 'contrib'
no previously-included directories found matching 'tasks'
no previously-included directories found matching 'tests'
creating /Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg
Extracting pip-9.0.1-py2.7.egg to /Library/Python/2.7/site-packages
Adding pip 9.0.1 to easy-install.pth file
Installing pip script to /usr/local/bin
Installing pip2.7 script to /usr/local/bin
Installing pip2 script to /usr/local/bin

Installed /Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg
Processing dependencies for pip
Finished processing dependencies for pip
```

14:24. Установил selenim командой

```
pip install selenium
```

и получил

```
Installing collected packages: selenium
Exception:
Traceback (most recent call last):
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/basecommand.py", line 215, in main
    status = self.run(options, args)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/commands/install.py", line 342, in run
    prefix=options.prefix_path,
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_set.py", line 784, in install
    **kwargs
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_install.py", line 851, in install
    self.move_wheel_files(self.source_dir, root=root, prefix=prefix)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_install.py", line 1064, in move_wheel_files
    isolated=self.isolated,
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/wheel.py", line 345, in move_wheel_files
    clobber(source, lib_dir, True)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/wheel.py", line 316, in clobber
    ensure_dir(destdir)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/utils/__init__.py", line 83, in ensure_dir
    os.makedirs(path)
  File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/os.py", line 157, in makedirs
    mkdir(name, mode)
OSError: [Errno 13] Permission denied: '/Library/Python/2.7/site-packages/selenium'
```

14:30 Загрузить Pyton с https://www.python.org/downloads/ и установить. Попробовать еще раз запустить 
```
sudo easy_install pip
```
14:38. Попробовать еще раз ввести
```
pip install selenium
```
Опять дерьмо:
```
Collecting selenium
  Using cached selenium-3.8.1-py2.py3-none-any.whl
Installing collected packages: selenium
Exception:
Traceback (most recent call last):
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/basecommand.py", line 215, in main
    status = self.run(options, args)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/commands/install.py", line 342, in run
    prefix=options.prefix_path,
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_set.py", line 784, in install
    **kwargs
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_install.py", line 851, in install
    self.move_wheel_files(self.source_dir, root=root, prefix=prefix)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/req/req_install.py", line 1064, in move_wheel_files
    isolated=self.isolated,
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/wheel.py", line 345, in move_wheel_files
    clobber(source, lib_dir, True)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/wheel.py", line 316, in clobber
    ensure_dir(destdir)
  File "/Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg/pip/utils/__init__.py", line 83, in ensure_dir
    os.makedirs(path)
  File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/os.py", line 157, in makedirs
    mkdir(name, mode)
OSError: [Errno 13] Permission denied: '/Library/Python/2.7/site-packages/selenium'
```
14:41. Установить [Java для mac](https://java.com/en/download/help/mac_install.xml), если нет.

14:43. Загрузить [Selenium Standalone Server](https://goo.gl/Lyo36k).

Пройти в папку с загруженным файлом jar и выполнить команду
```
java -jar selenium-server-standalone-3.0.1.jar
```
14:45. Установить [PyCharm](https://www.jetbrains.com/pycharm/download/#section=mac).

14:49. Создать новый проект, задав только имя - test.

14:51. Создать папку Part1 и в ней файл HelloWorld.py.

14:52. Вставить в файл код:
```
from selenium import webdriver

driver = webdriver.Firefox()
driver.get("http://www.python.org")
assert "Python" in driver.title
driver.close()
```
14:53. Запустить код. Fuck:
```
/Users/aleksey/PycharmProjects/test/venv/bin/python /Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py
Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py", line 1, in <module>
    from selenium import webdriver
ModuleNotFoundError: No module named 'selenium'

Process finished with exit code 1
```
14:56. Попробовать обновить PIP
```
pip install --upgrade pip
```
С pip все хорошо:
```
Requirement already up-to-date: pip in /Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg
```
15:01. Попробовать [вариант решения](https://stackoverflow.com/questions/40299451/error-while-installing-selenium-in-pip3):
```
sudo pip3 install -U selenium
```
15:02. Попробовать запустить тест. Получить на выходе
```
/Users/aleksey/PycharmProjects/test/venv/bin/python /Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py
Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py", line 1, in <module>
    from selenium import webdriver
ModuleNotFoundError: No module named 'selenium'

Process finished with exit code 1

Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py", line 1, in <module>
    from selenium import webdriver
ModuleNotFoundError: No module named 'selenium'
```
15:28. Fuck.

## День второй

12:41. Проверить версию (и состояние?) brew:

```
brew doctor
```

Выход:
```
Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry and just ignore them. Thanks!

Warning: "config" scripts exist outside your system or Homebrew directories.
`./configure` scripts often look for *-config scripts to determine if
software packages are installed, and what additional flags to use when
compiling and linking.

Having additional scripts in your path can confuse software installed via
Homebrew if the config script overrides a system or Homebrew provided
script of the same name. We found the following "config" scripts:
  /Library/Frameworks/Python.framework/Versions/3.6/bin/python3.6m-config
  /Library/Frameworks/Python.framework/Versions/3.6/bin/python3-config
  /Library/Frameworks/Python.framework/Versions/3.6/bin/python3.6-config
  /opt/local/bin/krb5-config
  /opt/local/bin/python2.7-config
  /opt/local/bin/curl-config
  /opt/local/bin/ncursesw6-config
  /opt/local/bin/apr-1-config
  /opt/local/bin/apu-1-config
  /opt/local/bin/pcre-config
  /opt/local/bin/ncurses6-config

Warning: Python is installed at /Library/Frameworks/Python.framework

Homebrew only supports building against the System-provided Python or a
brewed Python. In particular, Pythons installed to /Library can interfere
with other software installs.

Warning: You have MacPorts or Fink installed:
  /opt/local/bin/port

This can cause trouble. You don't have to uninstall them, but you may want to
temporarily move them out of the way, e.g.

  sudo mv /opt/local ~/macports

Warning: Unbrewed dylibs were found in /usr/local/lib.
If you didn't put them there on purpose they could cause problems when
building Homebrew formulae, and may need to be deleted.

Unexpected dylibs:
  /usr/local/lib/libtcl8.6.dylib
  /usr/local/lib/libtk8.6.dylib

Warning: Unbrewed header files were found in /usr/local/include.
If you didn't put them there on purpose they could cause problems when
building Homebrew formulae, and may need to be deleted.

Unexpected header files:
  /usr/local/include/tdbc.h
  /usr/local/include/mysqlStubs.h
  /usr/local/include/pqStubs.h
  /usr/local/include/tclOODecls.h
  /usr/local/include/itclTclIntStubsFcn.h
  /usr/local/include/itclIntDecls.h
  /usr/local/include/tcl.h
  /usr/local/include/itclMigrate2TclCore.h
  /usr/local/include/itcl.h
  /usr/local/include/tclThread.h
  /usr/local/include/tdbcInt.h
  /usr/local/include/tdbcDecls.h
  /usr/local/include/tclOO.h
  /usr/local/include/itcl2TclOO.h
  /usr/local/include/tk.h
  /usr/local/include/odbcStubs.h
  /usr/local/include/fakepq.h
  /usr/local/include/itclInt.h
  /usr/local/include/tkPlatDecls.h
  /usr/local/include/tclTomMathDecls.h
  /usr/local/include/tclTomMath.h
  /usr/local/include/fakemysql.h
  /usr/local/include/tclDecls.h
  /usr/local/include/tkDecls.h
  /usr/local/include/fakesql.h
  /usr/local/include/itclDecls.h
  /usr/local/include/tclPlatDecls.h

Warning: Unbrewed .pc files were found in /usr/local/lib/pkgconfig.
If you didn't put them there on purpose they could cause problems when
building Homebrew formulae, and may need to be deleted.

Unexpected .pc files:
  /usr/local/lib/pkgconfig/tcl.pc
  /usr/local/lib/pkgconfig/tk.pc

Warning: Unbrewed static libraries were found in /usr/local/lib.
If you didn't put them there on purpose they could cause problems when
building Homebrew formulae, and may need to be deleted.

Unexpected static libraries:
  /usr/local/lib/libtclstub8.6.a
  /usr/local/lib/libtkstub8.6.a

Warning: Broken symlinks were found. Remove them with `brew prune`:
  /usr/local/bin/apm
  /usr/local/bin/atom
```

12:53. Выполнить команду ```brew update```:

```
Updated Homebrew from b5529084 to 701ecb49.
Updated 2 taps (homebrew/core, caskroom/cask).
==> New Formulae
amber                        clingo                       field3d                      joplin                       monero                       qpid-proton                  spades
apm-server                   container-diff               genometools                  just                         mongodb@3.4                  qtkeychain                   sratoolkit
arcade-learning-environment  coreos-ct                    gifski                       kaitai-struct-compiler       mpir                         quicktype                    stress-ng
asciidoctor                  cp2k                         glances                      kallisto                     mrboom                       rawtoaces                    telnetd
auditbeat                    csvkit                       glslviewer                   kedge                        neal                         raylib                       terraform_landscape
augustus                     darksky-weather              go-jira                      keystone                     node@8                       rbenv-chefdk                 tmux-xpanes
avimetaedit                  ddgr                         go-statik                    kibana@5.6                   nopoll                       restic                       tnftp
ballerina                    diamond                      google-authenticator-libpam  kubeless                     nyx                          rst-lint                     tnftpd
bamtools                     dislocker                    gox                          kumo                         ocaml-findlib                rsync-time-backup            travis
bareos-client                dnsdist                      gutenberg                    lammps                       ocaml-num                    samtools                     unravel
bcftools                     docker-ls                    heartbeat                    libbitcoin-consensus         opencascade                  sceptre                      vcftools
bedops                       dps8m                        hlint                        libccd                       orocos-kdl                   seqtk                        vert
bedtools                     e2tools                      hmmer                        libidn2                      picard-tools                 shelltestrunner              vis
bioawk                       elasticsearch@5.6            htslib                       libjwt                       pinboard-notes-backup        shogun                       visp
blast                        elektra                      igv                          libtomcrypt                  pipenv                       sickle                       ydcv
bwa                          envconsul                    inspectrum                   libxo                        plank                        simg2img                     yq
chamber                      fastqc                       jabba                        mariadb-connector-odbc       prodigal                     singular                     zig
cling                        fbi-servefiles               jdupes                       mmseqs2                      pspg                         skafos                       zip
==> Updated Formulae
hugo ✔                       corsixth                     gjstest                      kvazaar                      mono-libgdiplus              povray                       stormlib
icu4c ✔                      coturn                       glade                        kyoto-tycoon                 monotone                     pow                          streamlink
node ✔                       couchdb                      glib                         kyua                         moreutils                    ppsspp                       strongswan
abcm2ps                      couchdb-lucene               glib-networking              lablgtk                      mosh                         pqiv                         stubby
abcmidi                      cppad                        glib-openssl                 lame                         mp3gain                      pre-commit                   stunnel
abnfgen                      cppcheck                     glide                        landscaper                   mpd                          prest                        subnetcalc
abyss                        cppcms                       global                       languagetool                 mpfi                         presto                       subversion
ace                          cpprestsdk                   glog                         lapack                       mpfr                         primesieve                   subversion@1.8
aces_container               cracklib                     glpk                         lastpass-cli                 mpg123                       prips                        suil
ack                          credstash                    gmic                         latexila                     mpich                        proguard                     suite-sparse
acmetool                     creduce                      gmime                        lbdb                         mplayershell                 prometheus                   sundials
acpica                       cromwell                     gmsh                         lcm                          mpv                          proof-general                superlu
adplug                       crosstool-ng                 gmt                          ldc                          mr                           protobuf                     supersonic
advancemame                  crowdin                      gmt@4                        ldns                         mruby                        protobuf-c                   suricata
adwaita-icon-theme           cryfs                        gnome-builder                lean-cli                     mu                           protobuf-swift               svgcleaner
afl-fuzz                     cryptopp                     gnome-doc-utils              leaps                        mujs                         protobuf@2.5                 svgo
agda                         crystal-icr                  gnome-recipes                ledger                       multimarkdown                psftools                     svtplay-dl
agedu                        crystal-lang                 gnu-smalltalk                ledit                        mupdf                        psqlodbc                     swagger-codegen
akamai                       csvtomd                      gnu-tar                      leiningen                    mupdf-tools                  pulledpork                   swfmill
alexjs                       ctop                         gnu-time                     lensfun                      mutt                         pumba                        swi-prolog
algernon                     cucumber-cpp                 gnu-units                    leptonica                    mvnvm                        pure-ftpd                    swift
allure                       curl                         gnumeric                     lgogdownloader               mycli                        purescript                   swift-protobuf
amazon-ecs-cli               cython                       gnupg                        libass                       mypy                         pushpin                      swiftformat
amqp-cpp                     czmq                         gnupg@2.0                    libassuan                    mysql                        pwntools                     swiftlint
angband                      dar                          gnuplot                      libatomic_ops                mysql++                      py2cairo                     sword
angular-cli                  datetime-fortran             gnuplot@4                    libbitcoin                   mysql-connector-c++          py3cairo                     sync_gateway
ansible                      datomic                      gnuradio                     libbitcoin-blockchain        mysql-sandbox                pybind11                     syncthing
ansible-cmdb                 davix                        gnutls                       libbitcoin-database          mysql@5.5                    pyenv                        sysbench
ansible-lint                 davmail                      go                           libbitcoin-explorer          mysql@5.6                    pygobject                    sysdig
ansifilter                   dbhash                       go@1.8                       libbitcoin-node              mytop                        pygobject3                   taisei
antigen                      dbus                         gobuster                     libbitcoin-server            nagios-plugins               pyinvoke                     taktuk
antlr                        dbus-glib                    godep                        libbluray                    nano                         pypy                         talloc
antlr4-cpp-runtime           dcm2niix                     goenv                        libcddb                      nanomsg                      pypy3                        tarantool
apache-arrow                 dcos-cli                     gofabric8                    libcdio                      nanopb-generator             pyqt                         task-spooler
apache-geode                 debianutils                  goffice                      libcdr                       nasm                         python                       tasksh
apache-opennlp               dehydrated                   gollum                       libcds                       natalie                      python-markdown              tbb
apache-spark                 dep                          gom                          libcello                     nativefier                   python3                      tcl-tk
apibuilder-cli               dependency-check             gomplate                     libconfig                    nats-streaming-server        pytouhou                     tclap
apktool                      devd                         goofys                       libcouchbase                 ncdu                         pyvim                        tectonic
app-engine-go-64             dhall-json                   google-benchmark             libcue                       ncmpc                        q                            telegraf
app-engine-java              dialog                       googler                      libdivecomputer              ncmpcpp                      qbs                          telegram-cli
apr                          diff-pdf                     goolabs                      libdvdcss                    nco                          qca                          teleport
apr-util                     diff-so-fancy                gopass                       libdvdnav                    ncurses                      qd                           temporal_tables
aptly                        diffoscope                   gosu                         libdvdread                   ncview                       qemu                         tenyr
arangodb                     digdag                       govendor                     libebur128                   ndpi                         qjackctl                     terminal-notifier
archivemount                 direnv                       gperftools                   libetonyek                   neko                         qmmp                         termius
argon2                       ditaa                        gpg-agent                    libfabric                    neovim                       qpdf                         terraform
argyll-cms                   django-completion            gpgme                        libfaketime                  nesc                         qrupdate                     terragrunt
aria2                        dlib                         gpsbabel                     libfixbuf                    net-snmp                     qscintilla2                  texapp
armadillo                    dmd                          gradle                       libfreehand                  netcdf                       qt                           texmath
armor                        dmtx-utils                   gradle-completion            libfreenect                  netpbm                       qtfaststart                  tfenv
arpack                       dnscrypt-proxy               grafana                      libgcrypt                    nettle                       quantlib                     tgui
artifactory                  docfx                        grails                       libgetdata                   nfdump                       quex                         thefuck
asciidoc                     docker                       grakn                        libgig                       nghttp2                      r                            thrift
asciinema                    docker-completion            graphicsmagick               libgit2-glib                 nginx                        rabbitmq                     thrift@0.9
asdf                         docker-compose               grc                          libgosu                      ngrep                        radamsa                      tidy-html5
aspcud                       docker-compose-completion    grib-api                     libgsf                       nickle                       radare2                      tig
aspectj                      docker-gen                   gromacs                      libgweather                  nifi                         rakudo-star                  tile38
assimp                       docker-machine-nfs           gron                         libhttpseverywhere           nikto                        rancher-cli                  tin
astyle                       doctl                        groonga                      libical                      nmh                          rancid                       tinc
at-spi2-atk                  doitlive                     groovysdk                    libjson-rpc-cpp              nnn                          ranger                       tintin
at-spi2-core                 doxygen                      grpc                         liblcf                       node-build                   ratfor                       tinyxml2
atlassian-cli                doxymacs                     gsmartcontrol                liblinear                    node@4                       rbenv-aliases                tippecanoe
ats2-postiats                dpkg                         gsoap                        liblunar                     node@6                       rbenv-binstubs               tmuxinator-completion
augeas                       druid                        gspell                       libmagic                     nodebrew                     rbenv-bundle-exec            tnef
aurora-cli                   dscanner                     gst-editing-services         libmaxminddb                 nomad                        rbenv-bundler                todoman
autogen                      dssim                        gst-libav                    libmicrohttpd                noti                         rbenv-bundler-ruby-version   tokei
aws-elasticbeanstalk         dub                          gst-plugins-bad              libmonome                    notmuch                      rbenv-communal-gems          tomcat
aws-sdk-cpp                  duck                         gst-plugins-base             libmpc                       nq                           rbenv-ctags                  tomcat-native
aws-shell                    dungeon                      gst-plugins-good             libmspub                     nrpe                         rbenv-default-gems           tor
awscli                       duplicity                    gst-plugins-ugly             libmwaw                      nsd                          rbenv-gemset                 tracebox
azure-cli                    dwarfutils                   gst-python                   libmxml                      nspr                         rbenv-use                    traefik
b2-tools                     dwdiff                       gst-rtsp-server              libogg                       nss                          rbenv-vars                   trafficserver
babl                         e2fsprogs                    gst-validate                 libopusenc                   ntl                          rbenv-whatis                 translate-shell
backupninja                  ecl                          gstreamer                    libpagemaker                 ntopng                       rclone                       transmission
bacula-fd                    efl                          gtk+                         libphonenumber               nuget                        rdfind                       treefrog
bam                          ejabberd                     gtk+3                        libpq                        numpy                        re2                          ttf2eot
bandcamp-dl                  elasticsearch                gtk-doc                      libpqxx                      nuttcp                       re2c                         ttfautohint
baresip                      elixir                       gtksourceview3               libpst                       nuxeo                        rebar@3                      tth
bartycrouch                  elvish                       gtkspell3                    libqalculate                 nvc                          recutils                     ttyd
basex                        emscripten                   gucharmap                    libquvi                      nvm                          redex                        ttyrec
bash                         encfs                        guile                        libraw                       ocaml                        redis                        twarc
bash-git-prompt              enchant                      guile@2.0                    librdkafka                   ocamlbuild                   redland                      twoping
bash-preexec                 enigma                       gwt                          libre                        ocamlsdl                     redpen                       twtxt
bash-snippets                entr                         gwyddion                     librealsense                 octave                       regex-opt                    txr
bazaar                       ephemeralpg                  gx                           libressl                     offlineimap                  remake                       txt2tags
bazel                        eralchemy                    gx-go                        librsvg                      ohcount                      reminiscence                 typescript
bchunk                       erlang                       gxml                         libsass                      ola                          reposurgeon                  u-boot-tools
bdw-gc                       erlang@18                    gzip                         libsigsegv                   omniorb                      resty                        ucon64
bear                         erlang@19                    h2o                          libsodium                    ompl                         rex                          udpxy
beast                        etcd                         hadolint                     libsoup                      oniguruma                    rgbds                        udunits
bench                        etsh                         hadoop                       libstfl                      onioncat                     riemann                      uftp
bento4                       exim                         hana                         libswiften                   onscripter                   ringojs                      uhd
bettercap                    exomizer                     haproxy                      libtasn1                     ooniprobe                    rocksdb                      unbound
betty                        expat                        harfbuzz                     libtcod                      opam                         rom-tools                    uncrustify
bfg                          exploitdb                    hashcat                      libtensorflow                open-babel                   root                         unixodbc
bibtexconv                   eye-d3                       hashpump                     libtiff                      open-mpi                     roswell                      unoconv
binaryen                     f3                           haskell-stack                libtins                      open-scene-graph             rpm                          upscaledb
bind                         faac                         haste-client                 libtorrent-rasterbar         openblas                     rsync                        urh
bindfs                       faad2                        haxe                         libtrace                     opencbm                      rtags                        urweb
binutils                     faas-cli                     hdf5                         libtrng                      opencoarrays                 rtv                          userspace-rcu
binwalk                      fabio                        hdf5@1.8                     libu2f-server                opencolorio                  ruby                         v8
biogeme                      fades                        heimdal                      libunistring                 opencv                       ruby-build                   vagrant-completion
bit                          fail2ban                     henplus                      libuv                        opencv@2                     ruby@1.9                     vala
bitcoin                      fantom                       hercules                     libvirt                      openfortivpn                 ruby@2.0                     vapoursynth
bitrise                      fb-client                    heroku                       libvisio                     openjazz                     ruby@2.1                     varnish
blackbox                     fcitx-remote-for-osx         hexgui                       libvoikko                    openmotif                    ruby@2.2                     varnish@4
blastem                      fd                           hfstospell                   libvpx                       openrtsp                     ruby@2.3                     vault
blink1                       fdclone                      hg-fast-export               libwebsockets                opensaml                     rust                         vault-cli
blockhash                    fdroidserver                 hg-flow                      libwpg                       openshift-cli                rustup-init                  vcdimager
bluepill                     feedgnuplot                  hh                           libwps                       openssl                      s-nail                       vdirsyncer
bmake                        feh                          highlight                    libxc                        openssl@1.1                  s-search                     veclibfort
boost                        ffmpeg                       hive                         libxkbcommon                 openttd                      s3fs                         verilator
boost-bcp                    ffmpeg@2.8                   hivemind                     libxml2                      openvdb                      s6                           vim
boost-build                  fftw                         hledger                      libxslt                      optipng                      sagittarius-scheme           vim@7.4
boost-mpi                    fibjs                        homebank                     libzdb                       opusfile                     saldl                        vips
boost-python                 file-roller                  html-xml-utils               lighttpd                     orc                          sassc                        voltdb
boost-python@1.59            filebeat                     htmlcleaner                  link-grammar                 orc-tools                    sbcl                         vowpal-wabbit
boost@1.55                   fio                          htmldoc                      linkerd                      ortp                         sbt                          vpcs
boost@1.57                   firebase-cli                 htop                         liquid-dsp                   osc                          sc-im                        vte
boost@1.59                   fish                         httest                       liquigraph                   oscats                       scalaenv                     vte3
boost@1.60                   fizmo                        http-server                  little-cms                   osm2pgrouting                scalapack                    vtk
bork                         flatbuffers                  httpd                        little-cms2                  osm2pgsql                    scalariform                  vultr
botan                        flatcc                       httpie                       lldpd                        osquery                      scalastyle                   w-calc
bowtie2                      flawfinder                   hubflow                      llnode                       osrm-backend                 scamper                      w3m
braid                        flow                         huexpress                    llvm                         ott                          sccache                      watson
brew-gem                     fluent-bit                   hwloc                        llvm@3.9                     overmind                     scipy                        weboob
brotli                       fluid-synth                  hydra                        llvm@4                       owfs                         scm-manager                  webp
bsponmpi                     flyway                       hyperscan                    log4cplus                    packer                       scons                        webpack
btfs                         fmt                          hypre                        logentries                   packetbeat                   scummvm                      websocketd
bubbros                      fn                           i2p                          logstash                     packetq                      scummvm-tools                weechat
buku                         fobis                        ib                           logtalk                      packmol                      sdl2                         wesnoth
bwfmetaedit                  folly                        ibex                         lsyncd                       paket                        sdl2_gfx                     wget
byobu                        fon-flash-cli                ice                          lua                          pandoc                       sdl2_mixer                   whatmp3
bzt                          fonttools                    icoutils                     lua@5.1                      pandoc-citeproc              sdl_mixer                    when
cabal-install                format-udf                   idnits                       lutok                        pandoc-crossref              sec                          whohas
cairo                        fossil                       idris                        lwtools                      pango                        securefs                     whois
cake                         fox                          imagemagick                  lxc                          paperkey                     selecta                      widelands
calabash                     fpc                          imagemagick@6                lynis                        par2                         selenium-server-standalone   wiggle
calc                         freeciv                      imagesnap                    lysp                         parallel                     serialosc                    wildfly-as
calcurse                     freediameter                 imapfilter                   lz4                          pari                         serveit                      wine
camlp4                       freeling                     immortal                     macosvpn                     pass                         sfcgal                       winetricks
camlp5                       freeradius-server            infer                        macvim                       passenger                    sfk                          wiredtiger
cargo-completion             freeswitch                   influxdb                     magic-wormhole               passpie                      shadowsocks-libev            wireguard-tools
carthage                     freetds                      innotop                      mailutils                    payara                       shairport-sync               wireshark
cask                         freetype                     inspircd                     mairix                       pazpar2                      shellcheck                   wolfssl
casperjs                     frugal                       instead                      makensis                     pcb                          shfmt                        wpcli-completion
cassandra@2.2                fswatch                      io                           mame                         pcl                          shibboleth-sp                wpscan
cayley                       fuse-emulator                iperf3                       mapnik                       pcsc-lite                    shmcat                       writerperfect
ccache                       fuse-zip                     ipfs                         mapserver                    pdal                         shocco                       wrk
ccm                          fuseki                       ipython                      mariadb                      pdf2htmlex                   shpotify                     wtf
ceres-solver                 fwup                         ipython@5                    mariadb-connector-c          pdfcrack                     shunit2                      wwwoffle
certbot                      fzf                          iron-functions               mariadb@10.0                 pdfpc                        shyaml                       wxpython
certigo                      galen                        ironcli                      mariadb@10.1                 pdftoedn                     sile                         x265
cfengine                     game-music-emu               irssi                        mas                          pdftoipe                     silk                         x3270
cfr-decompiler               gammaray                     isc-dhcp                     mat                          pdns                         simgrid                      xapian
cgal                         gammu                        iso-codes                    maven                        pdnsrec                      simple-obfs                  xcenv
cgrep                        gandi.cli                    ispc                         maxima                       peco                         sip                          xctool
chakra                       gauge                        itstool                      mdds                         pegtl                        sispmctl                     xmake
charm                        gawk                         jags                         mdp                          percona-server               sjk                          xml-tooling-c
charm-tools                  gcc                          jboss-forge                  media-info                   percona-server-mongodb       skinny                       xmoto
cheat                        gcc@4.9                      jena                         mediaconch                   percona-server@5.6           slackcat                     xmrig
check_postgres               gcc@5                        jenkins                      memcached                    percona-toolkit              smali                        xonsh
checkstyle                   gcc@6                        jenkins-job-builder          menhir                       percona-xtrabackup           smartmontools                xrootd
chibi-scheme                 gdal                         jenkins-lts                  mercurial                    pex                          smlnj                        xtensor
chicken                      gdbm                         jetty                        mesalib-glw                  pg_top                       snakemake                    xvid
chisel                       gdcm                         jetty-runner                 meson                        pgbouncer                    snapcraft                    xxhash
chromaprint                  gdnsd                        jfrog-cli-go                 mesos                        pgcli                        snappy                       yaf
chromedriver                 gearman                      jhiccup                      metabase                     pgloader                     snappystream                 yaml-cpp
chronograf                   geckodriver                  jhipster                     metaproxy                    pgplot                       snapraid                     yara
chuck                        gedit                        jing-trang                   metricbeat                   pgpool-ii                    sngrep                       yarn
cimg                         geeqie                       jmxtrans                     mg                           pgroonga                     snort                        yash
citus                        gegl                         joe                          mgba                         pgrouting                    socat                        yaz
cjdns                        generate-json-schema         jpeg-turbo                   micro                        phoronix-test-suite          solr                         yaze-ag
ckan                         geoip                        jruby                        micropython                  physfs                       sonarqube                    yeti
clamav                       geoipupdate                  json-fortran                 midnight-commander           pianod                       sops                         ykman
clang-format                 geoserver                    jsoncpp                      mighttpd2                    pick                         source-highlight             ykpers
clhep                        get-flash-videos             jsvc                         mikutter                     picocom                      source-to-image              yle-dl
clinfo                       get_iplayer                  juju                         miller                       pigz                         sourcekitten                 you-get
clipper                      getdns                       juju-wait                    mimic                        pike                         sourcery                     youtube-dl
clojure                      geth                         jump                         mingw-w64                    pilosa                       spdlog                       yubico-piv-tool
cloog                        getmail                      kafka                        minimal-racket               pinentry                     speech-tools                 z3
closure-compiler             gexiv2                       kapacitor                    minio                        pioneer                      sphinx                       z80dasm
cmake                        ghc                          karn                         minio-mc                     pioneers                     sphinx-doc                   zabbix
cmark                        ghi                          keepassc                     miniupnpc                    pius                         spigot                       zanata-client
cmark-gfm                    gibo                         kerl                         minizinc                     pjproject                    spin                         zbackup
cnats                        gifsicle                     keychain                     mitie                        planck                       sql-translator               zbar
cockatrice                   gimme                        khal                         mitmproxy                    plantuml                     sqlcipher                    zebra
cockroach                    gist                         khard                        mkclean                      platformio                   sqldiff                      zenity
cocoapods                    git                          kibana                       mkdocs                       plplot                       sqlite                       zero-install
cocot                        git-annex                    kitchen-sync                 mksh                         plzip                        sqlite-analyzer              zeromq
codemod                      git-cinnabar                 kite                         mkvalidator                  pmd                          sqlmap                       zile
coffeescript                 git-cola                     knot                         mkvtoolnix                   pngquant                     squashfs                     zimg
collectd                     git-crypt                    knot-resolver                mlt                          poco                         src                          zint
collector-sidecar            git-ftp                      kobalt                       mockserver                   pod2man                      ssdeep                       zmqpp
commandbox                   git-integration              kompose                      moco                         polyml                       ssh-audit                    znc
compcert                     git-remote-hg                konoha                       modd                         ponyc                        sshguard                     zookeeper
conan                        git-review                   kontena                      modules                      ponysay                      sslh                         zorba
conjure-up                   git-secret                   kops                         molecule                     poppler                      sslmate                      zplug
consul                       git-town                     kotlin                       monetdb                      postgis                      sslscan                      zpython
consul-template              gitbucket                    kpcli                        mongo-c-driver               postgres-xc                  sslsplit                     zsh
convmv                       gitg                         krb5                         mongodb                      postgresql                   sslyze                       zsh-autosuggestions
convox                       github-keygen                kube-aws                     mongoose                     postgresql@9.4               statik                       zsh-lovers
coq                          gitlab-runner                kubectx                      monit                        postgresql@9.5               stern                        zstd
corebird                     gitup                        kubernetes-cli               monitoring-plugins           postgresql@9.6               stockfish                    zurl
coreutils                    gjs                          kubernetes-helm              mono                         postgrest                    stoken
==> Renamed Formulae
camlistore -> perkeep                    findbugs -> spotbugs                     newsbeuter -> newsboat                   ssreflect -> math-comp                   tachyon -> alluxio
==> Deleted Formulae
angolmois                         docker@1.11                       gsl@1                             juju@1.25                         mg3a                              ppl@0.11
antlr@3                           docker@1.71                       gst-plugins-bad@0.10              kubernetes-cli@1.3                mongodb@2.6                       qt@5.7
apache-spark@1.5                  eigen@3.2                         gst-plugins-base@0.10             laszip@2                          moodbar                           redis@2.6
apache-spark@1.6                  gcc@4.6                           gst-plugins-good@0.10             ledger@2.6                        mpfr@2                            selenium-server-standalone@2.45
autoconf@2.64                     gcc@4.7                           gst-plugins-ugly@0.10             libical-glib                      mvptree                           srtp@1.6
automake@1.12                     gcc@4.8                           gstreamer@0.10                    libmpc@0.8                        open-mpi@1.6                      stklos
azure-cli@1                       geogit                            influxdb@0.8                      libpng@1.2                        otto                              swig@2
bazel@0.2                         glfw@2                            isl@0.11                          libpqxx@3                         pcap_dnsproxy                     talk-filters
clang-format@3.8                  gmp@4                             isl@0.12                          libxml2@2.7                       percona-server@5.5                unison@2.40
clasp                             go@1.5                            isl@0.14                          litmus                            perl@5.14                         zeromq@3.2
cloog@0.15                        grails@2.5                        jetty@8                           logstash@2.4                      pond                              zeromq@4.0
cloudbees-sdk                     gringo                            jpeg@6                            lua@5.3                           ponscripter-sekai                 zeromq@4.1
```

12:58. Используя pip установить Selenium командой ```pip install selenium```:

```
Requirement already satisfied: selenium in /Library/Python/2.7/site-packages
```

13:02. Сохранить в файл python_org_search.py и выполнить команду ```python python_org_search.py``` для данных:

```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

driver = webdriver.Firefox()
driver.get("http://www.python.org")
assert "Python" in driver.title
elem = driver.find_element_by_name("q")
elem.send_keys("pycon")
elem.send_keys(Keys.RETURN)
assert "No results found." not in driver.page_source
driver.close()
```

13:09. Найти инструкцию как в PyCharm создать проект для тестирования. [Например](https://pythonworld.ru/osnovy/pycharm-python-tutorial.html). Установить [PyCharm Edu](https://www.jetbrains.com/pycharm-edu/download/#section=mac). В Complete Installation выбрать вариант Do not import settings. В диалоге "Are you a Learner or a Educator" выбрать Learner. В Welcome to PyCharm выбрать Browse Courses > Introduction to Python > new virtual env 3.6.4

13:17. Ввести свое имя в строку и запустить код ```print("Hello, world! My name is Aleksey")```

13:24. Запустить код

```
from selenium import webdriver

driver = webdriver.Firefox()
driver.get("http://www.python.org")
assert "Python" in driver.title
driver.close()
```

Получить

```
/Users/aleksey/PycharmProjects/test/venv/bin/python /Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py
Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/test/Part1/HelloWorld.py", line 1, in <module>
    from selenium import webdriver
ModuleNotFoundError: No module named 'selenium'

Process finished with exit code 1
```

13:28. Посмотреть [подсказку на StackOverflow](https://stackoverflow.com/questions/18868743/how-to-install-selenium-webdriver-on-mac-os) и ... 

13:33. Обратиться к книге Learning Selenium Testing Tools with Python. На 15 странице получить рекомендации. Создать проект setests. В опции New enviroment using "Virtualenv", в Base interpreter выбрать вариант "/usr/bin/python2.7".

13:43. Создать New Python File. Ввести и запустить код:

```
from selenium import webdriver

# create a new Firefox session
driver = webdriver.Firefox()
driver.implicitly_wait(30)
driver.maximize_window()

# navigate to the application home page
driver.get("http://demo.magentocommerce.com/")

# get the search textbox
search_field = driver.find_element_by_name("q")
search_field.clear()

# enter search keyword and submit
search_field.send_keys("phones")
search_field.submit()

# get all the anchor elements which have product names displayed
# currently on result page using find_elements_by_xpath method
products = driver.find_elements_by_xpath("//h2[@class='product-name']/a")

# get the number of anchor elements found
print "Found " + str(len(products)) + " products:"

# iterate through each anchor element and print the text that is
# name of the product
for product in products:
    print product.text

# close the browser window
driver.quit()
```

Получить:

```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/searchproducts.py
Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/setests/searchproducts.py", line 1, in <module>
    from selenium import webdriver
ImportError: No module named selenium

Process finished with exit code 1

13:50. Запустить из консоли PyCharm install selenium
Collecting selenium
  Using cached selenium-3.8.1-py2.py3-none-any.whl
Installing collected packages: selenium
Successfully installed selenium-3.8.1
```

13:52. [Загрузить ChromeDriver](https://chromedriver.storage.googleapis.com/index.html?path=2.35/).

13:55 Запустить из консоли PyCharm команду типа ```java -jar selenium-server-standalone-3.8.1.jar```, переделав в путь до нахождения файла на машине - ```java -jar /Users/aleksey/Downloads/selenium-server-standalone-3.8.1.jar``` и получить:

```
13:57:39.323 INFO - Selenium build info: version: '3.8.1', revision: '6e95a6684b'
13:57:39.324 INFO - Launching a standalone Selenium Server
2018-02-02 13:57:39.727:INFO::main: Logging initialized @1159ms to org.seleniumhq.jetty9.util.log.StdErrLog
13:57:39.851 INFO - Using `new FirefoxOptions()` is preferred to `DesiredCapabilities.firefox()`
13:57:39.896 INFO - Using `new ChromeOptions()` is preferred to `DesiredCapabilities.chrome()`
13:57:39.908 INFO - Using `new EdgeOptions()` is preferred to `DesiredCapabilities.edge()`
13:57:39.912 INFO - Driver class not found: com.opera.core.systems.OperaDriver
13:57:39.912 INFO - Using `new OperaOptions()` is preferred to `DesiredCapabilities.operaBlink()`
13:57:39.916 INFO - Using `new SafariOptions()` is preferred to `DesiredCapabilities.safari()`
13:57:39.918 INFO - Driver class not found: org.openqa.selenium.phantomjs.PhantomJSDriver
13:57:40.014 INFO - Driver provider class org.openqa.selenium.ie.InternetExplorerDriver registration is skipped:
 registration capabilities Capabilities {browserName: internet explorer, ensureCleanSession: true, platform: WINDOWS, version: } does not match the current platform MAC
13:57:40.015 INFO - Driver provider class org.openqa.selenium.edge.EdgeDriver registration is skipped:
 registration capabilities Capabilities {browserName: MicrosoftEdge, platform: WINDOWS, version: } does not match the current platform MAC
13:57:40.135 INFO - Using `new ChromeOptions()` is preferred to `DesiredCapabilities.chrome()`
13:57:40.136 INFO - Using `new EdgeOptions()` is preferred to `DesiredCapabilities.edge()`
13:57:40.136 INFO - Using `new FirefoxOptions()` is preferred to `DesiredCapabilities.firefox()`
13:57:40.137 INFO - Using `new OperaOptions()` is preferred to `DesiredCapabilities.operaBlink()`
13:57:40.137 INFO - Using `new SafariOptions()` is preferred to `DesiredCapabilities.safari()`
13:57:40.161 INFO - Using the passthrough mode handler
2018-02-02 13:57:40.246:INFO:osjs.Server:main: jetty-9.4.7.v20170914
2018-02-02 13:57:40.303:WARN:osjs.SecurityHandler:main: ServletContext@o.s.j.s.ServletContextHandler@353352b6{/,null,STARTING} has uncovered http methods for path: /
2018-02-02 13:57:40.310:INFO:osjsh.ContextHandler:main: Started o.s.j.s.ServletContextHandler@353352b6{/,null,AVAILABLE}
2018-02-02 13:57:40.394:INFO:osjs.AbstractConnector:main: Started ServerConnector@aba625{HTTP/1.1,[http/1.1]}{0.0.0.0:4444}
2018-02-02 13:57:40.395:INFO:osjs.Server:main: Started @1826ms
13:57:40.395 INFO - Selenium Server is up and running
```

14:07. Запустить тест и получить:

```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/searchproducts.py
Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/setests/searchproducts.py", line 4, in <module>
    driver = webdriver.Chrome()
  File "/Users/aleksey/PycharmProjects/setests/venv/lib/python2.7/site-packages/selenium/webdriver/chrome/webdriver.py", line 68, in __init__
    self.service.start()
  File "/Users/aleksey/PycharmProjects/setests/venv/lib/python2.7/site-packages/selenium/webdriver/common/service.py", line 83, in start
    os.path.basename(self.path), self.start_error_message)
selenium.common.exceptions.WebDriverException: Message: 'chromedriver' executable needs to be in PATH. Please see https://sites.google.com/a/chromium.org/chromedriver/home


Process finished with exit code 1
```

15:46. https://stackoverflow.com/questions/43528944/python-browser-with-mac-error-chromedriver-executable-needs-to-be-in-path brew install chromedriver

```
Updating Homebrew...
==> Auto-updated Homebrew!
Updated Homebrew from 701ecb49 to a44b21b2.
Updated 2 taps (homebrew/core, caskroom/cask).
==> New Formulae
gocryptfs
==> Updated Formulae
amber                            app-engine-java                  docfx                            faas-cli                         git-imerge                       snapcraft

==> Downloading https://chromedriver.storage.googleapis.com/2.35/chromedriver_mac64.zip
######################################################################## 100.0%
==> Caveats
To have launchd start chromedriver now and restart at login:
  brew services start chromedriver
Or, if you don't want/need a background service you can just run:
  chromedriver
==> Summary
🍺  /usr/local/Cellar/chromedriver/2.35: 4 files, 11.3MB, built in 3 seconds
(venv) MacBook-Air-Aleksey:setests aleksey$ 
```

15:49. Запустить тест и получить новое сообщение:

```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/searchproducts.py
Traceback (most recent call last):
  File "/Users/aleksey/PycharmProjects/setests/searchproducts.py", line 14, in <module>
    search_field = driver.find_element_by_name("q")
  File "/Users/aleksey/PycharmProjects/setests/venv/lib/python2.7/site-packages/selenium/webdriver/remote/webdriver.py", line 487, in find_element_by_name
    return self.find_element(by=By.NAME, value=name)
  File "/Users/aleksey/PycharmProjects/setests/venv/lib/python2.7/site-packages/selenium/webdriver/remote/webdriver.py", line 955, in find_element
    'value': value})['value']
  File "/Users/aleksey/PycharmProjects/setests/venv/lib/python2.7/site-packages/selenium/webdriver/remote/webdriver.py", line 312, in execute
    self.error_handler.check_response(response)
  File "/Users/aleksey/PycharmProjects/setests/venv/lib/python2.7/site-packages/selenium/webdriver/remote/errorhandler.py", line 237, in check_response
    raise exception_class(message, screen, stacktrace)
selenium.common.exceptions.NoSuchElementException: Message: no such element: Unable to locate element: {"method":"name","selector":"q"}
  (Session info: chrome=63.0.3239.132)
  (Driver info: chromedriver=2.35.528157 (4429ca2590d6988c0745c24c8858745aaaec01ef),platform=Mac OS X 10.13.0 x86_64)


Process finished with exit code 1
```

16:00. Вырезать

```
# get the search textbox
search_field = driver.find_element_by_name("q")
search_field.clear()

# enter search keyword and submit
search_field.send_keys("phones")
search_field.submit()

# get all the anchor elements which have product names displayed
# currently on result page using find_elements_by_xpath method
products = driver.find_elements_by_xpath("//h2[@class='product-name']/a")

# get the number of anchor elements found
print "Found " + str(len(products)) + " products:"

# iterate through each anchor element and print the text that is
# name of the product
for product in products:
    print product.text
```

16:04. Запустить ставший код:
```
from selenium import webdriver

# driver = webdriver.Chrome()

# create a new Firefox session
driver = webdriver.Chrome()
driver.implicitly_wait(30)
driver.maximize_window()

# navigate to the application home page
driver.get("http://demo.magentocommerce.com/")

driver.find_element_by_class_name('dropdown-toggle').click()

# close the browser window
driver.quit()
```
И получить на выходе:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/searchproducts.py

Process finished with exit code 0
```

Успех.

02.02.2018.
