# GradeTest

Unit Testing sample programme code for learning purpose

## Project Environment

### Required Softwares & Tools:
	1.Eclipse CDT
	2.MSYS2 (includes MinGW + cppunittest){hint: no extra MinGW and msys required}
		
### Instructions for Installation:

**Download Install MSYS2(MinGw)**
Follow this Instruction:  
https://msys2.github.io/  
It's tested with the MSYS2 64Bit Variant with the 32 Bit Compiler.
Install nesessary packages
Install mingw toolchain
Open the MinGw Shell:
pacman -S base-devel git mercurial cvs wget p7zip
pacman -S perl ruby python2 mingw-w64-i686-toolchain
PATH= C:\msys64\mingw32\bin;C:\msys64\usr\bin;
Install Qt
pacman -S mingw-w64-i686-qt4

**Install QtCreator installation**

Download and execute the Installationbinary:

https://download.qt.io/snapshots/qtcreator/3.6.0-rc1/latest/qt-creator-opensource-windows-x86-3.6.0-rc1.exe

**Install Boost**
`pacman -S mingw-w64-i686-boost`
`Install MAKE`
`pacman -S make`

**Install CppUnit**
``pacman -S mingw-w64-i686-cppunit``
``Install Lcov``
``cd /tmp/``
``git clone https://github.com/linux-test-project/lcov.git``
``cd lcov/``
``make install``

**Install cppcheck**
git clone https://github.com/danmar/cppcheck.git
cd cppcheck
Im Makefile die Zeile
'#RDYNAMIC=-rdynamic'
auskommentieren
make SRCDIR=build CFGDIR=/usr/share/cppcheck/ LDFLAGS=-lshlwapi
make install SRCDIR=build CFGDIR=/usr/share/cppcheck/ LDFLAGS=-lshlwapi

**Install gcovr**
pip install gcovr

**Install sqlitewrapped**
cvs checkout -d sqlitewrapped LIBS\CPP\00006_sqlitewrapped
cd sqlitewrapped
make
make install

**Install paho**
git clone https://github.com/eclipse/paho.mqtt.c.git
copy the paho_mqtt_mingw.patch into the folder
cd paho.mqtt.c
git apply paho_mqtt_mingw.patch
Umgebungsvariable setzen
MSYS2 = 1


## known errors and soluations(Optional)

- **ERROR**:cppunit path not included or giving error related to that 
	
- **Soln**:
	
		a) check the installation for cppunit testing framework and MSYS2	
		b) check system path variables setup