# GradeTest

Unit Testing sample programme code for learning purpose

## Project Environment

### Required Softwares & Tools:
	1.Eclipse CDT
	2.MSYS2 (includes MinGW + cppunittest){hint: no extra MinGW and msys required}
		
### Instructions for Installation:

**Download Install MSYS2(MinGw)**

https://msys2.github.io/<br>
It's tested with the MSYS2 64Bit Variant with the 32 Bit Compiler.
Install nesessary packages
Install mingw toolchain
Open the MinGw Shell:<br>
pacman -S base-devel git mercurial cvs wget p7zip<br>
pacman -S perl ruby python2 mingw-w64-i686-toolchain<br>
PATH= C:\msys64\mingw32\bin;C:\msys64\usr\bin;<br>
Install Qt<br>
pacman -S mingw-w64-i686-qt4<br>

**Install QtCreator installation**

Download and execute the Installationbinary:<br>
https://download.qt.io/snapshots/qtcreator/3.6.0-rc1/latest/qt-creator-opensource-windows-x86-3.6.0-rc1.exe

**Install Boost**<br>
`pacman -S mingw-w64-i686-boost`<br>
`Install MAKE`<br>
`pacman -S make`

**Install CppUnit**<br>
``pacman -S mingw-w64-i686-cppunit``<br>
``Install Lcov``<br>
``cd /tmp/``<br>
``git clone https://github.com/linux-test-project/lcov.git``<br>
``cd lcov/``<br>
``make install``

**Install cppcheck**<br>
``git clone https://github.com/danmar/cppcheck.git``<br>
``cd cppcheck``<br>
Im Makefile die Zeile'#RDYNAMIC=-rdynamic'auskommentieren<br>
``make SRCDIR=build CFGDIR=/usr/share/cppcheck/ LDFLAGS=-lshlwapi``<br>
``make install SRCDIR=build CFGDIR=/usr/share/cppcheck/ LDFLAGS=-lshlwapi``

**Install gcovr**<br>
``pip install gcovr``

**Install sqlitewrapped**<br>
``cvs checkout -d sqlitewrapped LIBS\CPP\00006_sqlitewrapped``<br>
``cd sqlitewrapped``<br>
``make``<br>
``make install``

**Install paho**<br>
``git clone https://github.com/eclipse/paho.mqtt.c.git``<br>
copy the paho_mqtt_mingw.patch into the folder<br>
``cd paho.mqtt.c``<br>
``git apply paho_mqtt_mingw.patch``<br>
Umgebungsvariable setzen 'MSYS2 = 1'


## known errors and soluations(Optional)

- **ERROR**:cppunit path not included or giving error related to that 	
- **Soln**:
	
		a) check the installation for cppunit testing framework and MSYS2	
		b) check system path variables setup
