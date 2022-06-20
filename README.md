# API-final-project
Welcome to the github page of final Project for Audio Processing and Indexing. Music and images are adjacent forms of art, each carrying and presenting information through a different medium. The transformation of one such medium into another and obtaining a new representation of the same information is thus an interesting prospect. One such example is that of synaesthesia, a rare condition where some individuals are able to visualize sound in certain forms of the condition. This phenomenon is used as inspiration for the project, where we implement a music analyzer that is able to detect the key and tempo and is able to transcribe individual notes in a given song, and this information is used to create a visualization that is based on the phenomenon of synaesthesia.

## Website
The project also has a website: https://api-final-project.vercel.app/

## Installing Requirements
### Python Packages
- `librosa`
- `ffmpeg`
### System Libraries/Tools
- `podman`

## Key and Tempo Detection
To run the key and tempo detection, open the "BPM and Key Detection.ipynb" Jupyter Notebook and just run all. You will need librosa installed. Also required to have ffmpeg installed so that `audioread` can read `.mp3` files.

## Music Transcription
The notebook "Automatic Music Transcription.ipynb" is a slightly modified version of the example notebook which can be found on https://music-and-culture-technology-lab.github.io/omnizart-doc/quick-start.html. As the original notebook is run in Google Colab, our implementation should also be run in Google Colab.

## Music Visualization
The notebook "Synesthetizer.ipynb" contains the code for the visualization. Cells should be run one by one.


