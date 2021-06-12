# US-domestic flight analysis

This project is to analyse the US flight information and simple prediction of arrival delay

To Build docker container and run the analysis inside

    export DOCKER_BUILDKIT=0
    export COMPOSE_DOCKER_CLI_BUILD=0
    
    poetry export -f requirements.txt -o requirements.txt --without-hashes
    
    docker build -t container .
    docker run -it -p 8888:8888 container

To start running jupyter notebook inside the container

    Jupyter notebook stop 8888

To copy the files from the container to lcoal

    docker cp bold_leavitt:/analysis.ipynb ./analysis.ipynb 
