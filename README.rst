1. LINUX ARM NANO PI NEO PLUS 2
===================

.. code:: python

    sudo apt update
    sudo apt install python3.9
    sudo apt-get install python3-dev python3-pip
    sudo -H pip3 install -U pip numpy
    sudo apt install cmake
    pip install opencv-python
    pip install requests
    apt install libgl1-mesa-glx

1.1. **COMPILAR**

.. code:: python

    wget http://dlib.net/files/dlib-19.24.tar.bz2
    tar xvf dlib-19.24.tar.bz2
    cd dlib-19.24/
    mkdir build
    cd build
    cmake ..
    cmake --build . --config Release
    sudo make install
    sudo ldconfig
    cd ..
    pkg-config --libs --cflags dlib-1

1.2. **INSTALAR NO PYTHON**

.. code:: python

    cd dlib-19.9
    sudo python3 setup.py install

**OPCIONAL**
===================

.. code:: python

    sudo pip3 install virtualenv virtualenvwrapper
    echo "# Virtual Environment Wrapper" >> ~/.bashrc
    echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc
    source ~/.bashrc

    # create virtual environment
    mkvirtualenv ml-py3 -p python3
    workon ml-py3
     
    # now install python libraries within this virtual environment
    pip install numpy scipy matplotlib scikit-image scikit-learn ipython
     
    # if you want to install dlib from pip
    pip install dlib
     
    # else if you have compiled from source move to dlib's root directory
    cd dlib-19.9
    python setup.py install
     
    # quit virtual environment
    deactivate
