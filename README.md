# API-final-project
Welcome to the github page of final Project for Audio Processing and Indexing. Music and images are adjacent forms of art, each carrying and presenting information through a different medium. The transformation of one such medium into another and obtaining a new representation of the same information is thus an interesting prospect. One such example is that of synaesthesia, a rare condition where some individuals are able to visualize sound in certain forms of the condition. This phenomenon is used as inspiration for the project, where we implement a music analyzer that is able to detect the key and tempo and is able to transcribe individual notes in a given song, and this information is used to create a visualization that is based on the phenomenon of synaesthesia.

## Website
The project also has a website: https://api-final-project.vercel.app/

## Installation Requirements
### Python Packages
- `librosa`
- `ffmpeg`
### System Libraries/Tools
- `podman` - a light-weight alternative to Docker
    - https://podman.io/getting-started/installation
- Alternatively, Docker can also be used

## Key and Tempo Detection
To run the key and tempo detection, open the "BPM and Key Detection.ipynb" Jupyter Notebook and just run all. You will need librosa installed. Also required to have ffmpeg installed so that `audioread` can read `.mp3` files.

## Music Transcription
The notebook "Automatic Music Transcription.ipynb" is a slightly modified version of the example notebook which can be found on https://music-and-culture-technology-lab.github.io/omnizart-doc/quick-start.html. As the original notebook is run in Google Colab, our implementation should also be run in Google Colab.

## Music Visualization
Before running the code in the notebook, the neural-style docker image needs to be pulled to the system. Provided podman is installed, this can be done with: 
`podman pull docker.io/ffedoroff/neural-style`

'podman' can be replaced with 'docker' in the above statement if Docker is being used instead of podman.

The notebook "Synesthetizer.ipynb" contains the code for the visualization. Cells should be run one by one. In the final section, a shell command is run to spin up a container using podman. This can be run directly from the notebook. Alternatively, if Docker is being used, the command below can be run - 

`docker run -v <DIRECTORY>/Outputs:/out -it ffedoroff/neural-style th neural_style.lua -gpu -1 -style_image Grid_artistic.png -content_image <pattern-map-image>.png`

Replace 'pattern-map-image' with the respective image name from the 'Outputs' directory

An example visualization created for the following song - https://www.youtube.com/watch?v=QbeHq1CLqJ8 is shown below: 

![alt text](Example_Visualization.png?style-centerme "Visualization for Apres Moi")


