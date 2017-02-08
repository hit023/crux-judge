# Running Instructions

## Developers

0. Follow the [install](docs/install.md) instructions

1. To start the Django Local Server, run the following commands:

```bash
cd ~/crux-judge
source env/bin/activate
python3 judge/manage.py runserver
```

Check if the localserver is working, by opening your browser and typing `127.0.0.1:8000`
If you see the Django Congratulations message, you have successfully run the server!

2. To test file uploading, go to `127.0.0.1:8000/trial/`
Select a file to upload, then click on submit to upload the file
To confirm a successful upload, check in `crux-judge/src/server/submissions`.

If you see your file present, congrats! You've successfully uploaded a file to the server!
If not, PLEASE open an issue on the GitHub repo!

# Testing/Tweaking Instructions

## Developers

* [Py file for compile+execute function, step1.py](judge/trial/step1.py)
Note that [step1.py](judge/trial/step1.py) is a stand-alone file, unrelated to django
It just contains the handler function, nothing more (move it according to project structure, if need be)

To test the working of the file,
+ create a [hello_world.c](judge/trial/step1.py) test file with `gedit judge/trial/hello_world.c` 
+ open test1.py with `gedit judge/trial/step1.py` to see the handler function
+ to test the [file](judge/trial/step1.py), run the following command:
`python3 judge/trial/step1.py`

