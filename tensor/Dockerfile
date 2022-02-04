FROM tensorflow/tensorflow:2.0.3-py3-jupyter

RUN apt-get update
RUN apt-get upgrade -y
RUN pip3 install --upgrade pip

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.token=", "--NotebookApp.base_url=/jupy2", "--allow-root"]