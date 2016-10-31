**1. Clone wallet sources**

```
git clone https://github.com/BEASTLICK-INTERNET-POLICY-COMMISSION/bipcoinwallet.git
```


**2. Create git submoduleat the same level as `src`. For example:**

```
git submodule add https://github.com/BEASTLICK-INTERNET-POLICY-COMMISSION/bipcoin.git cryptonote
git submodule update --init -- "cryptonote"
```

**3 (Linux). Build**

```
mkdir build && cd build && cmake .. && make
```

**3 (Windows). Build**

Dependencies: MSVC 2013 or later, CMake 2.8.6 or later, Boost 1.55, Qt 5.7. You may download them from:
http://www.microsoft.com/
http://www.cmake.org/
http://www.boost.org/
https://www.qt.io/

```
cmake -G "Visual Studio 12" -DCMAKE_PREFIX_PATH=C:\Qt\5.7\msvc2013
```
This will create a bipcoin.sln file which you can open in Visual Studio and build.

**4 (Windows). Additional Files Required**

For Windows, some QT files are also required. Copy the following from Qt to the BipCoin executable folder:

From C:\Qt\5.7\msvc2013\bin:
```
Qt5Core.dll
Qt5Gui.dll
Qt5Widgets.dll
```
From C:\Qt\5.7\msvc2013\plugins\platforms
```
platforms\qwindows.dll
```
If you are making a debug build you will need the altenatives to the above files which end in 'd', Like Qt5Coded.dll instead of Qt5Code.dll

The Folder structure should look like this:
```
Directory of C:\bipcoin
         1,742,336 bipcoin.exe
        77,163,152 cryptonote.lib
        <DIR>          platforms
         4,673,536 Qt5Core.dll
         4,868,096 Qt5Gui.dll
         4,486,656 Qt5Widgets.dll

 Directory of C:\bipcoin\platforms
           988,160 qwindows.dll
```
