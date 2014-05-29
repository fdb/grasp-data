Grasp Data
==========
MongoDB database dump for the "Comparing visual and textual programming approaches for data visualisation" paper, submitted to GPCE'14.

To access the data, install [MongoDB](http://www.mongodb.org/) first. On OS X, we prefer [Homebrew](http://brew.sh/):

    ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
    brew update
    brew install mongodb

Run the MongoDB server:

    mongod

Then, in another shell, restore the data from the data set:

    git clone git://github.com/fdb/grasp-data
    cd grasp-data
    mongorestore

Notebook
========
In addition to the data we've also provided the calculations performed to convert discrete events into durations. This is included as an [IPython notebook](http://ipython.org/notebook.html).

To run, assuming you're already in the grasp-data directory:

    sudo easy_install virtualenv
    virtualenv .
    source bin/activate
    export CFLAGS=-Qunused-arguments
    export CPPFLAGS=-Qunused-arguments
    pip install -r requirements.txt
    ipython notebook
