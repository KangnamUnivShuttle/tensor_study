FROM armswdev/tensorflow-arm-neoverse:r22.01-tf-2.7.0-eigen

RUN sudo apt-get update
RUN sudo apt-get install python3-matplotlib=3.1.2-1ubuntu4 -y

RUN sudo apt-get install libfreetype6-dev=2.10.1-2ubuntu0.1 libfreetype-dev=2.10.1-2ubuntu0.1 -y
RUN sudo apt-get install pkg-config=0.29.1-0ubuntu4 -y
RUN sudo apt-get install cython=0.29.14-0.1ubuntu3 -y

RUN sudo apt-get remove python3 -y
RUN sudo apt-get install python3=3.8.2-0ubuntu2 -y

RUN sudo apt-get remove python3-pip -y
RUN sudo apt-get install python3-pip -y

RUN python3 -V
RUN pip3 -V

RUN curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
RUN python3 get-pip.py --force-reinstall

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.base_url=/jupy2", "--allow-root"]
