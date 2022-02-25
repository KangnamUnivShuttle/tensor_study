FROM tensorflow/tensorflow:2.0.3-py3-jupyter

RUN apt-get update
RUN apt-get upgrade -y
RUN pip3 install --upgrade pip

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

RUN pip3 install openpyxl==3.0.9

RUN apt-get install git -y
RUN pip3 install git+https://github.com/ssut/py-hanspell.git

RUN pip3 install konlpy==0.6.0
RUN pip3 install git+https://github.com/lovit/customized_konlpy.git
RUN apt install default-jdk -y

RUN pip3 install nltk==3.6.7

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.token=", "--NotebookApp.base_url=/jupy2", "--allow-root"]