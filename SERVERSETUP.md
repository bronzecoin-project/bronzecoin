# Server Setup on Linux

1. Update and upgrade your system:

    ```bash
    sudo apt-get update && sudo apt-get upgrade
    ```

2. Build Dependency

    - Install essential build tools and libraries:

        ```bash
        sudo apt-get install build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 libssl-dev
        sudo apt-get install libevent-dev libboost-system-dev libboost-filesystem-dev libboost-test-dev libboost-thread-dev libfmt-dev libssl-dev
        sudo apt-get install libdb++-dev libdb-dev libsqlite3-dev libminiupnpc-dev libzmq3-dev
        ```

3. GUI Dependency

    - Install required GUI libraries:

        ```bash
        sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools
        sudo apt-get install libqrencode-dev
        ```

4. Berkeley DB Installation

    - Install Berkeley DB:

        ```bash
        ./contrib/install_db4.sh `pwd`
        ```

5. Build

    - Build the server:

        ```bash
        ./autogen.sh
        ./configure
        make
        make install # optional
        ```
