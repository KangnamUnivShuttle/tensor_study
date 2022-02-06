FROM armswdev/tensorflow-arm-neoverse:r22.01-tf-2.7.0-eigen

RUN apt-get update
RUN apt-get install python-dev -y

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.base_url=/jupy2", "--allow-root"]
