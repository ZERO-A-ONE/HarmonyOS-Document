# Setting Up a Development Environment<a name="EN-US_TOPIC_0000001054022306"></a>

## Environment Requirements<a name="section1724111409282"></a>

## Hardware<a name="section185788208272"></a>

-   Linux server
-   Windows workstation \(host computer\)
-   Hi3518EV300 IoT camera development board
-   USB cable and network cable \(The Windows workstation is connected to Hi3518EV300 development board through the USB cable and network cable.\)

    [Figure 1](#fig8211468392)  shows the hardware connections.


**Figure  1**  Hardware connections<a name="fig8211468392"></a>  
![](figures/hardware-connections-1.png "hardware-connections-1")

## Software<a name="section383442213405"></a>

**Table  1**  Platforms required for the Hi3518EV300 development board

<a name="table16641975408"></a>
<table><thead align="left"><tr id="row196634713405"><th class="cellrowborder" valign="top" width="8.53%" id="mcps1.2.5.1.1"><p id="p116632718408"><a name="p116632718408"></a><a name="p116632718408"></a>Hardware</p>
</th>
<th class="cellrowborder" valign="top" width="11.66%" id="mcps1.2.5.1.2"><p id="p1766312724017"><a name="p1766312724017"></a><a name="p1766312724017"></a>Software</p>
</th>
<th class="cellrowborder" valign="top" width="66%" id="mcps1.2.5.1.3"><p id="p666327144010"><a name="p666327144010"></a><a name="p666327144010"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="13.81%" id="mcps1.2.5.1.4"><p id="p106631273406"><a name="p106631273406"></a><a name="p106631273406"></a>Remarks</p>
</th>
</tr>
</thead>
<tbody><tr id="row066315717402"><td class="cellrowborder" valign="top" width="8.53%" headers="mcps1.2.5.1.1 "><p id="p666318712403"><a name="p666318712403"></a><a name="p666318712403"></a>Linux compile server</p>
</td>
<td class="cellrowborder" valign="top" width="11.66%" headers="mcps1.2.5.1.2 "><p id="p76632712403"><a name="p76632712403"></a><a name="p76632712403"></a>Operating system</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.5.1.3 "><p id="p15663127204015"><a name="p15663127204015"></a><a name="p15663127204015"></a>Ubuntu 16.04 64-bit or later is used for the Linux OS, and bash is used as the shell.</p>
<div class="note" id="note196631578401"><a name="note196631578401"></a><a name="note196631578401"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p1466311720406"><a name="p1466311720406"></a><a name="p1466311720406"></a>Common software such as samba and vim is installed in the OS by default. Adaptation is required to support Linux file sharing.</p>
</div></div>
</td>
<td class="cellrowborder" rowspan="2" valign="top" width="13.81%" headers="mcps1.2.5.1.4 "><p id="p96631975404"><a name="p96631975404"></a><a name="p96631975404"></a>You can develop programs on the Windows workstation or on the Linux server through remote login.</p>
</td>
</tr>
<tr id="row19664272408"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1366314764011"><a name="p1366314764011"></a><a name="p1366314764011"></a>Windows workstation</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p15663177204019"><a name="p15663177204019"></a><a name="p15663177204019"></a>Operating system</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p1766411719408"><a name="p1766411719408"></a><a name="p1766411719408"></a>Windows XP/Windows7/Windows10</p>
</td>
</tr>
</tbody>
</table>

## Build Tools for Linux<a name="section11111412465"></a>

The following table describes the common tools required for Linux and how to obtain them.

**Table  2**  Development tools and obtaining methods

<a name="en-us_topic_0000001054501981_table6299192712513"></a>
<table><thead align="left"><tr id="en-us_topic_0000001054501981_row122993276512"><th class="cellrowborder" valign="top" width="13.081308130813083%" id="mcps1.2.4.1.1"><p id="en-us_topic_0000001054501981_p1829914271858"><a name="en-us_topic_0000001054501981_p1829914271858"></a><a name="en-us_topic_0000001054501981_p1829914271858"></a>Development Tool</p>
</th>
<th class="cellrowborder" valign="top" width="19.921992199219922%" id="mcps1.2.4.1.2"><p id="en-us_topic_0000001054501981_p429918274517"><a name="en-us_topic_0000001054501981_p429918274517"></a><a name="en-us_topic_0000001054501981_p429918274517"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="66.996699669967%" id="mcps1.2.4.1.3"><p id="en-us_topic_0000001054501981_p12997271757"><a name="en-us_topic_0000001054501981_p12997271757"></a><a name="en-us_topic_0000001054501981_p12997271757"></a>How to Obtain</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0000001054501981_row430016273514"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p330015271158"><a name="en-us_topic_0000001054501981_p330015271158"></a><a name="en-us_topic_0000001054501981_p330015271158"></a>Python3.7+</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p43003270510"><a name="en-us_topic_0000001054501981_p43003270510"></a><a name="en-us_topic_0000001054501981_p43003270510"></a>Runs the compilation scripts.</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p18254155164617"><a name="en-us_topic_0000001054501981_p18254155164617"></a><a name="en-us_topic_0000001054501981_p18254155164617"></a><a href="https://www.python.org/ftp/python/3.8.5/Python-3.8.5.tgz" target="_blank" rel="noopener noreferrer">https://www.python.org/ftp/python/3.8.5/Python-3.8.5.tgz</a></p>
</td>
</tr>
<tr id="en-us_topic_0000001054501981_row42668197206"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p426711912014"><a name="en-us_topic_0000001054501981_p426711912014"></a><a name="en-us_topic_0000001054501981_p426711912014"></a>bash</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p14267131962014"><a name="en-us_topic_0000001054501981_p14267131962014"></a><a name="en-us_topic_0000001054501981_p14267131962014"></a>Executes commands.</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p14267101962014"><a name="en-us_topic_0000001054501981_p14267101962014"></a><a name="en-us_topic_0000001054501981_p14267101962014"></a>Internet</p>
</td>
</tr>
<tr id="en-us_topic_0000001054501981_row1711946154018"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p15588165684216"><a name="en-us_topic_0000001054501981_p15588165684216"></a><a name="en-us_topic_0000001054501981_p15588165684216"></a>gn</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p4588135634213"><a name="en-us_topic_0000001054501981_p4588135634213"></a><a name="en-us_topic_0000001054501981_p4588135634213"></a>Generates ninja compilation scripts.</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p10572194318318"><a name="en-us_topic_0000001054501981_p10572194318318"></a><a name="en-us_topic_0000001054501981_p10572194318318"></a><a href="https://repo.huaweicloud.com/harmonyos/compiler/gn/1523/linux/gn.1523.tar" target="_blank" rel="noopener noreferrer">https://repo.huaweicloud.com/harmonyos/compiler/gn/1523/linux/gn.1523.tar</a></p>
</td>
</tr>
<tr id="en-us_topic_0000001054501981_row16990164213404"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p1858825613428"><a name="en-us_topic_0000001054501981_p1858825613428"></a><a name="en-us_topic_0000001054501981_p1858825613428"></a>ninja</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p15844174611816"><a name="en-us_topic_0000001054501981_p15844174611816"></a><a name="en-us_topic_0000001054501981_p15844174611816"></a>Executes ninja compilation scripts.</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p1923373393515"><a name="en-us_topic_0000001054501981_p1923373393515"></a><a name="en-us_topic_0000001054501981_p1923373393515"></a><a href="https://repo.huaweicloud.com/harmonyos/compiler/ninja/1.9.0/linux/ninja.1.9.0.tar" target="_blank" rel="noopener noreferrer">https://repo.huaweicloud.com/harmonyos/compiler/ninja/1.9.0/linux/ninja.1.9.0.tar</a></p>
</td>
</tr>
<tr id="en-us_topic_0000001054501981_row192161027104010"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p15217227174016"><a name="en-us_topic_0000001054501981_p15217227174016"></a><a name="en-us_topic_0000001054501981_p15217227174016"></a>LLVM</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p122171727184019"><a name="en-us_topic_0000001054501981_p122171727184019"></a><a name="en-us_topic_0000001054501981_p122171727184019"></a>Functions as the compiler toolchain.</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p0191147134415"><a name="en-us_topic_0000001054501981_p0191147134415"></a><a name="en-us_topic_0000001054501981_p0191147134415"></a><a href="https://repo.huaweicloud.com/harmonyos/compiler/clang/9.0.0-34042/linux/llvm-linux-9.0.0-34042.tar" target="_blank" rel="noopener noreferrer">https://repo.huaweicloud.com/harmonyos/compiler/clang/9.0.0-34042/linux/llvm-linux-9.0.0-34042.tar</a></p>
</td>
</tr>
<tr id="en-us_topic_0000001054501981_row18516509507"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p14521650135017"><a name="en-us_topic_0000001054501981_p14521650135017"></a><a name="en-us_topic_0000001054501981_p14521650135017"></a>hc-gen</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p125255010501"><a name="en-us_topic_0000001054501981_p125255010501"></a><a name="en-us_topic_0000001054501981_p125255010501"></a>Configures and compiles files.</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p145061517114519"><a name="en-us_topic_0000001054501981_p145061517114519"></a><a name="en-us_topic_0000001054501981_p145061517114519"></a><a href="https://repo.huaweicloud.com/harmonyos/compiler/hc-gen/0.65/linux/hc-gen-0.65-linux.tar" target="_blank" rel="noopener noreferrer">https://repo.huaweicloud.com/harmonyos/compiler/hc-gen/0.65/linux/hc-gen-0.65-linux.tar</a></p>
</td>
</tr>
<tr id="en-us_topic_0000001054501981_row105773499422"><td class="cellrowborder" valign="top" width="13.081308130813083%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0000001054501981_p15300102717517"><a name="en-us_topic_0000001054501981_p15300102717517"></a><a name="en-us_topic_0000001054501981_p15300102717517"></a>IPOP, PuTTY, or other HyperTerminal software</p>
</td>
<td class="cellrowborder" valign="top" width="19.921992199219922%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0000001054501981_p109418530386"><a name="en-us_topic_0000001054501981_p109418530386"></a><a name="en-us_topic_0000001054501981_p109418530386"></a>Connects to the Linux server (choose one of the terminals).</p>
</td>
<td class="cellrowborder" valign="top" width="66.996699669967%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0000001054501981_p7312122523813"><a name="en-us_topic_0000001054501981_p7312122523813"></a><a name="en-us_topic_0000001054501981_p7312122523813"></a>Internet (for example, <a href="https://www.putty.org/" target="_blank" rel="noopener noreferrer">https://www.putty.org/</a>)</p>
</td>
</tr>
</tbody>
</table>

## Development Tools for Windows<a name="section11161833102716"></a>

**Table  3**  Development tools for the Windows workstation

<a name="table1313323311274"></a>
<table><thead align="left"><tr id="row3133133312711"><th class="cellrowborder" valign="top" width="16.371637163716375%" id="mcps1.2.4.1.1"><p id="p16132203372716"><a name="p16132203372716"></a><a name="p16132203372716"></a>Development Tool</p>
</th>
<th class="cellrowborder" valign="top" width="37.04370437043704%" id="mcps1.2.4.1.2"><p id="p1413219339278"><a name="p1413219339278"></a><a name="p1413219339278"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="46.58465846584659%" id="mcps1.2.4.1.3"><p id="p17133183312711"><a name="p17133183312711"></a><a name="p17133183312711"></a>How to Obtain</p>
</th>
</tr>
</thead>
<tbody><tr id="row13697410143219"><td class="cellrowborder" valign="top" width="16.371637163716375%" headers="mcps1.2.4.1.1 "><p id="p163612016916"><a name="p163612016916"></a><a name="p163612016916"></a>Visual Studio Code</p>
</td>
<td class="cellrowborder" valign="top" width="37.04370437043704%" headers="mcps1.2.4.1.2 "><p id="p1563690791"><a name="p1563690791"></a><a name="p1563690791"></a>Edits code.</p>
</td>
<td class="cellrowborder" valign="top" width="46.58465846584659%" headers="mcps1.2.4.1.3 "><p id="p146361701097"><a name="p146361701097"></a><a name="p146361701097"></a><a href="https://code.visualstudio.com/" target="_blank" rel="noopener noreferrer">https://code.visualstudio.com/</a></p>
</td>
</tr>
<tr id="row12133123315277"><td class="cellrowborder" valign="top" width="16.371637163716375%" headers="mcps1.2.4.1.1 "><p id="p613393317271"><a name="p613393317271"></a><a name="p613393317271"></a>HiTool</p>
</td>
<td class="cellrowborder" valign="top" width="37.04370437043704%" headers="mcps1.2.4.1.2 "><p id="p201334121092"><a name="p201334121092"></a><a name="p201334121092"></a>Burns the images and the U-boot.</p>
</td>
<td class="cellrowborder" valign="top" width="46.58465846584659%" headers="mcps1.2.4.1.3 "><p id="p2014134844017"><a name="p2014134844017"></a><a name="p2014134844017"></a><a href="http://www.hihope.org/download/AllDocuments" target="_blank" rel="noopener noreferrer">http://www.hihope.org/download/AllDocuments</a></p>
<p id="p141194824119"><a name="p141194824119"></a><a name="p141194824119"></a>Tool package: Hi3516-Hitool.zip</p>
</td>
</tr>
</tbody>
</table>

## Installing the Basic Compilation Environment<a name="section7813043104310"></a>

## Connecting to a Linux Server<a name="section111021456154718"></a>

Using PuTTY to log in to a Linux server from a PC running Windows

1.  Open  [PuTTY](https://www.putty.org/), enter the IP address of the Linux server, and click  **Open**.

    **Figure  2**  PuTTY configuration<a name="en-us_topic_0000001054501981_en-us_topic_0000001054781998_f825e6d7569cc487db9b744e454c7157a"></a>  
    ![](figures/putty-configuration.png "putty-configuration")

2.  Click  **Yes**  in the PuTTY  **Security Alert**  dialog box.
3.  Enter the account and password.

    **Figure  3**  Login<a name="en-us_topic_0000001054501981_en-us_topic_0000001054781998_fe1428afffbdd45f9b4a39497691ff5ff"></a>  
    ![](figures/login.png "login")

4.  The login is successful.

    **Figure  4**  Successful login<a name="en-us_topic_0000001054501981_en-us_topic_0000001054781998_f11bea69483e14bd39fef4a10b1ed1a3a"></a>  
    ![](figures/successful-login.png "successful-login")


## Changing Linux Shell to Bash<a name="section980212574810"></a>

Run the following command to check whether bash is used as the shell:

```
ls -l /bin/sh
```

If  **/bin/sh -\> bash**  is not displayed, do as follows to change shell to bash.

**Method 1:**  Run the following command on the device and then click  **No**.

```
sudo dpkg-reconfigure dash
```

**Method 2:**  Run the  **rm -rf /bin/sh**  command to delete sh and then run the sudo  **ln -s /bin/bash /bin/sh**  command to create a new soft link.

```
sudo rm -rf /bin/sh
sudo ln -s /bin/bash /bin/sh
```

## Installing a Python Environment<a name="section918195118487"></a>

1.  Start a Linux server.
2.  Run the following command to check the Python version \(Python 3.7 or later is required\):

    ```
    python3 --version
    ```

    Do as follows to install Python, for example, Python 3.8.

    1.  Run the following command to check the Ubuntu version:

    ```
    cat /etc/issue
    ```

    1.  Install Python based on the Ubuntu version.
        -   If the Ubuntu version is 18 or later, run the following command:

            ```
            sudo apt-get install python3.8
            ```

        -   If the Ubuntu version is 16, download the installation package and install Python.

            1.  Run the following command to install Python environment dependencies \(gcc, g++, make, zlib, libffi\):

            ```
            sudo apt-get install gcc && sudo apt-get install g++ && sudo apt-get install make && sudo apt-get install zlib* && sudo apt-get install libffi-dev
            ```

            1.  Obtain the  [Python3.8.5 installation package](https://www.python.org/ftp/python/3.8.5/Python-3.8.5.tgz), save it to the Linux server, and run the following command:

            ```
            tar -xvzf Python-3.8.5.tgz && cd Python-3.8.5 && sudo ./configure && sudo make && sudo make install
            ```



3.  After Python is installed, run the following command to link the Python path to  **/usr/bin/python**:

    ```
    which python3.8
    cd /usr/bin && sudo rm python && sudo ln -s /usr/local/bin/python3.8 python && python --version
    ```

4.  Install and upgrade the Python package management tool \(pip3\) using either of the following methods:
    -   **Command line:**

        ```
        sudo apt-get install python3-setuptools python3-pip -y
        sudo pip3 install --upgrade pip
        ```

    -   **Installation package:**

        ```
        curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
        python get-pip.py
        ```


5.  Run the following command to install setuptools:

    ```
    pip3 install setuptools
    ```

6.  Install the GUI menuconfig tool \(Kconfiglib\). You are advised to install Kconfiglib 13.2.0 or later.
    -   **Command line:**

        ```
        sudo pip3 install kconfiglib
        ```


    -   **Installation package:**
        1.  Download the .whl file \(for example,  **kconfiglib-13.2.0-py2.py3-none-any.whl**\).

            Download path:  [https://pypi.org/project/kconfiglib\#files](https://pypi.org/project/kconfiglib#files)


        1.  Run the following command to install the .whl file:

            ```
            sudo pip3 install kconfiglib-13.2.0-py2.py3-none-any.whl
            ```




## Installing a File Packing Tool<a name="section145881557185214"></a>

1.  Start a Linux server.
2.  Run the following command to install  **dosfstools**.

    ```
    sudo apt-get install dosfstools
    ```

3.  Run the following command to install  **mtools**.

    ```
    sudo apt-get install mtools
    ```


## Installing Compilation Tools<a name="section7227629152013"></a>

>![](public_sys-resources/icon-notice.gif) **NOTICE:** 
>-   If you obtain the source code using an HPM component or HPM CLI tool, compilation tools like  **gn**,  **ninja**,  **LLVM**, and  **hc-gen**  are not required.
>-   \(Recommended\) If you obtain the source code through an image site or a code repository, compilation tools like  **gn**,  **ninja**,  **LLVM**, and  **hc-gen**  need to be installed.
>    When installing  **gn**,  **ninja**,  **LLVM**, and  **hc-gen**, ensure that the environment variable paths of the compilation tools are unique.

## Installing gn<a name="section119641436125219"></a>

1.  Start a Linux server.
2.  Download  [gn](https://repo.huaweicloud.com/harmonyos/compiler/gn/1523/linux/gn.1523.tar).
3.  Run the following command to decompress the gn installation package to  **\~/gn**.

    ```
    tar -xvf gn.1523.tar -C ~/
    ```

4.  Set an environment variable by performing the following steps. Open the  **\~/.bashrc**  file in Vim first.

    ```
    vim ~/.bashrc
    ```

    Copy the following command to the last line of the  **.bashrc**  file, save the file, and exit.

    ```
    export PATH=~/gn:$PATH
    ```

5.  Run the following command to validate the environment variable.

    ```
    source ~/.bashrc
    ```


## Installing ninjah<a name="section96781928145213"></a>

1.  Start a Linux server.
2.  Download  [ninja](https://repo.huaweicloud.com/harmonyos/compiler/ninja/1.9.0/linux/ninja.1.9.0.tar).
3.  Run the following command to decompress the ninja installation package to  **\~/ninja**.

    ```
    tar -xvf ninja.1.9.0.tar -C ~/
    ```

4.  Set an environment variable by performing the following steps. Open the  **\~/.bashrc**  file in Vim first.

    ```
    vim ~/.bashrc
    ```

    Copy the following command to the last line of the  **.bashrc**  file, save the file, and exit.

    ```
    export PATH=~/ninja:$PATH
    ```

5.  Run the following command to validate the environment variable.

    ```
    source ~/.bashrc
    ```


## Installing the LLVM Toolchain<a name="section667822819521"></a>

1.  Start a Linux server.
2.  Download  [LLVM](http://tools.harmonyos.com/mirrors/clang/9.0.0-34042/linux/llvm-linux-9.0.0-34042.tar).
3.  Run the following command to decompress the LLVM installation package to  **\~/llvm**.

    ```
    tar -xvf llvm-linux-9.0.0-34042.tar -C ~/
    ```

4.  Set an environment variable by performing the following steps. Open the  **\~/.bashrc**  file in Vim first.

    ```
    vim ~/.bashrc
    ```

    Copy the following command to the last line of the  **.bashrc**  file, save the file, and exit.

    ```
    export PATH=~/llvm/bin:$PATH
    ```

5.  Run the following command to validate the environment variable.

    ```
    source ~/.bashrc
    ```


##  Installing hc-gen<a name="section201517625210"></a>

1.  Start a Linux server.
2.  Download  [hc-gen](https://repo.huaweicloud.com/harmonyos/compiler/hc-gen/0.65/linux/hc-gen-0.65-linux.tar).
3.  Run the following command to decompress the hc-gen installation package to  **\~/hc-gen**  on the Linux server.

    ```
    tar -xvf hc-gen-0.65-linux.tar -C ~/
    ```

4.  Set an environment variable by performing the following steps. Open the  **\~/.bashrc**  file in Vim first.

    ```
    vim ~/.bashrc
    ```

    Copy the following command to the last line of the  **.bashrc**  file, save the file, and exit.

    ```
    export PATH=~/hc-gen:$PATH
    ```

5.  Run the following command to validate the environment variable.

    ```
    source ~/.bashrc
    ```


