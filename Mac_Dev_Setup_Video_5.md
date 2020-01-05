# Video 5: Developer Environment Setup
Youtube Link: https://youtu.be/hXfegfi824k

### Python
* Timestamp: 1.30 - 25.20

* Install pyenv
    ```bash
    brew install pyenv
    ```

* Install python 3.6.5
    ```bash
    pyenv install 3.6.5
    ```
* Setting python global version
    ```bash
    pyenv global 3.6.5
    ```

* pyenv init
    ```bash
    eval "$(pyenv init -)"
    ```
* Install virtualenv
    ```bash
    pip install --user virtualenv
    ```
  
* Create a virtual env
    ```bash
    python -m venv sandbox
    ```
  
* Activate virtual env
    ```bash
    source ~/Development/virtual_env/sandbox/bin/activate
    ```
  
* Deactivate virtual env
    ```bash
    deactivate
    ```

### Git
* Timestamp: 25.40 - 32.10

* Generate RSA key
    ```bash
    sss-keygen -t rsa
    ```

* Copy public key
    ```bash
    pbcopy < ~/.ssh/id_rsa.pub
    ```

### Docker
* Timestamp: 32.34 - 46.45

* Install link: https://www.docker.com/

* Docker clean up script
    ```bash
    #!/bin/sh
    
    echo "Cleaning out all docker files";
    docker images;
    docker rm -r $(docker ps -a -q);
    docker rmi -f $(docker images -q);
    echo "Removed all docker files";
    ```
  
* Add exe
    ```bash
    chmod +x fry_docker.sh
    ```
  
* Alias
    ```bash
    # user alias
    alias fry_docker="~/Development/dev_tools/scripts/fry_docker.sh"
    ```

### Java
* Timestamp: 46.44 - 53.25

* Install link: https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html

### nvm, node and a little react
* Timestamp: 54.00 - 1.02.20

* Install script
    ```bash
    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
    ```

* zshrc goodies if needed
    ```bash
    export NVM_DIR="/Users/jdaigle/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    ```
  
* Install node
    ```bash
    nvm install --lts
    ```
  
* Create react app
    ```bash
    npm install -g create-react-app
    npx create-react-app sb_app 
    ```
  
* Starting react app
    ```bash
    cd sb_app
    npm start
    ```