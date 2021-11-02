FROM python:3.7.6
ENV SOURCE_PATH /curso
WORKDIR $SOURCE_PATH
COPY Pipfile* $SOURCE_PATH/

COPY . .

RUN pip install pipenv
RUN pip install jupyter
RUN pipenv install --dev
RUN pipenv install ipykernel
RUN pipenv run python -m ipykernel install --user --name='libropython'
