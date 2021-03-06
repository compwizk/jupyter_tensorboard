FROM jupyter/tensorflow-notebook

COPY . /opt/jupyter-tensorboard
USER root
RUN cd /opt/jupyter-tensorboard \
    && python3 setup.py install \
    && fix-permissions $CONDA_DIR \
    && fix-permissions /home/$NB_USER
USER $NB_UID