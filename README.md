CV Project

Running Instructions

This project was creating with Python 3.6 and has not been tested with other versions. It may
work with later versions, but please run with Python 3.6 to ensure success.

Requirements for this project are managed with Pipenv. To install Pipenv, run the following:

`pip install pipenv`

The project also requires Protobuf on the system. On Mac, you can install Protobuf with Homebrew:

`brew install protobuf`

The project was developed for Mac, though it should run on another system so long as Protobuf can
be properly installed. You can test that Protobuf is installed by running:

`protoc`

If you recieve a usage message, then it has been installed properly.

Now that the system is prepared, navigate to the project top directory:

`cd part2`

Running the object detection network requires the tensorflow model repository installed locally. While
in the top-level directory, run:

`git clone https://github.com/tensorflow/models.git`

Navigate into the tensorflow model repo, run the protoc command, and navigate back to the top-level:

`cd models/research`
`protoc object_detection/protos/*.proto --python_out=.`
`cd ../..`

Next, we can install all the Python requirements with Pipenv

`pipenv install`

Now we can actually run the detection:

`pipenv run python ./detect_image.py`

