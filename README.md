
<div align="center">
	<h1 align="center">
	🧑‍⚕️<br />
COVID-19 DETECTOR AI
	</h1>
	<span>
	Deep CNN based AI app for COVID Diagnosis using Chest X-Rays
	</span>
</div>


### Live Demo : [Heroku Web App](https://covid-diagniosis-ai.herokuapp.com)
## Tech Stack
- PyTorch (DL Model)
- OpenCV 
- Flask (Backend)
- Gunicorn Server
- Heroku (PaaS)

## Instruction
#### To run locally,
1) Clone this repository with `git clone`.
2) Open a terminal inside the project directory.
3) Install dependencies using `pip install -r requirements.txt`
3) Run `python app.py` to open the app on `localhost:5000`.
#### To Deploy on Heroku 
> Deploying in heroku is bit of a hectic process involves a lot of bug fixing. I hope I can guide you through it. 
> Since I used PyTorch and OpenCV in my app, heroku needs some pre-configuration.

1) Make sure you have all the requirements in `requirements.py`
> I assume you have already created heroku account and Heroku CLI on your machine. If not, follow this  [tutorial](https://devcenter.heroku.com/start).
2) Open a terminal on the project directory and create a heroku application using `heroku create covid19-xray-detector`
3) Since I use OpenCV Contrib Library, it requires `libsm6 libxender1` and it can be installed only though `apt-get`. So we import buildpack in heroku, use `heroku buildpacks:add --index 1 heroku-community/apt`.
4) Create Aptfile, refer [this](https://github.com/Saranmanoharan511/covid-19-diagnosis/blob/main/Aptfile)
5) Now you are all set to go, deploy with a single command `git push heroku master`.

