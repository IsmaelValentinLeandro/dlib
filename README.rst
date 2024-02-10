LINUX ARM
===================
``sudo apt update``
``sudo apt install python3.9``
``sudo apt-get install python3-dev python3-pip``
``sudo -H pip3 install -U pip numpy``
``sudo apt install cmake``
``pip install opencv-python``
``pip install requests``
``apt install libgl1-mesa-glx``

**COMPILAR**
===================
``wget http://dlib.net/files/dlib-19.24.tar.bz2``
``tar xvf dlib-19.24.tar.bz2``
``cd dlib-19.24/``
``mkdir build``
``cd build``
``cmake ..
``cmake --build . --config Release``
``sudo make install``
``sudo ldconfig``
``cd ..``
``pkg-config --libs --cflags dlib-1``


**INSTALAR NO PYTHON**
===================
``cd dlib-19.9``
``sudo python3 setup.py install``

**OPCIONAL**
===================
``sudo pip3 install virtualenv virtualenvwrapper``
``echo "# Virtual Environment Wrapper" >> ~/.bashrc``
``echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc``
``source ~/.bashrc``
``mkvirtualenv dlib -p python3``
``workon dlib ``
``pip3 install numpy scipy matplotlib scikit-image scikit-learn ipython``
``deactivate``
