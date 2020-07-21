FROM continuumio/anaconda3:latest

RUN conda create -n QISKIT_ENV python=3
RUN conda init bash
RUN activate QISKIT_ENV

RUN conda install jupyter -y
RUN pip --default-timeout=100 install gevent
RUN pip install qiskit
RUN pip install qiskit[visualization]

RUN mkdir /opt/notebooks

CMD /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip 0.0.0.0 --port=8888 --no-browser --allow-root
