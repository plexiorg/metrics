# metrics
doing it the right way


## Getting started

To install docker & compose:

    sudo apt install apt-transport-https ca-certificates curl
    curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
    # add docker
    echo "deb [arch=armhf] https://download.docker.com/linux/debian jessie stable" | sudo tee /etc/apt/sources.list.d/docker.list
    # add docker-compose for service installer files
    echo "deb https://packagecloud.io/Hypriot/Schatzkiste/debian/ jessie main" | sudo tee /etc/apt/sources.list.d/hypriot.list
    # add hypriot keys
    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 37BBEE3F7AD95B3F
    sudo apt update
    sudo apt install docker-ce docker-compose
