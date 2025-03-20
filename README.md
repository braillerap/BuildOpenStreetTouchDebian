# BuildOpenStreetTouchDebian
A docker configuration to build OpenStreetTouch for debian base os

# usage

## building docker image
    export HOST_UID=$(id -u)
    export HOST_GID=$(id -g)

    docker build  UID=$HOST_UID --build-arg GID=$HOST_GID -t buildopenstreettouchdebian .

## use docker image to build DesktopBrailleRAP
    docker run --rm -it --name openstreettouch_debian_build -e BRANCH_BUILD=<branch|main> -v ./dist/:/home/builduser/dist buildopenstreettouchdebian
