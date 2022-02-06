FROM tensorflow/tensorflow:2.0.3-py3-jupyter

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.base_url=/jupy2", "--allow-root"]
