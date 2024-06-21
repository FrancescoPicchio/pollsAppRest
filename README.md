My Polls app realized with Django REST API and a very very simple React app. 

I had problems with git because I had to restructure the directories in order to make it possible to do the deployment on Heroku, and in the process the repository stopped tracking folders and commits just didn't work
I'm sorry about this but it was the only way.

TO RUN THIS LOCALLY:

The back-end part of the application with django rest api and there is a requirements.txt file so that it's easier to install all the necessary libraries. There is an .env file in back-end/django_rest_api
that should be set to the localhost/port used for the react app.

The front-end part of the application can be initialized with npm run install and unfortunately to make it work locally you have to modify API_URL in the javascript files in front-end/src/services,
for api.jsx you need to insert your localhost link and then add at the end /api/ (sorry I forgot to adjust this because I was running late), while in auth.jsx instead of only /api/ you need to add /api/auth/ 
to your link. To run the front end use npm run dev.

DESCRIPTION OF THE APP:

The backend was realized with Django REST API, using the models Question and Choice, and providing endpoints to view all the questions, view a singular question with all its details, create a question,
create a choice for a question and submit a vote for a particular choice of a question. Also there is token authentication.

The frontend was done with a very very simple React app (created using Vite) using axios and react-router-dom libraries to make use of the endpoints provided by the Django REST API. I didn't have enough time to make it prettier
with bootstrap and such, and unfortunately when deleting questions you have to reload the page to show that it was actually deleted. 

LINK TO DEPLOYED APPLICATIONS:

Front-end (which is connected to the back-end):
  https://polls-app-client-ppm-feaeb624ad75.herokuapp.com

Back-end (doesn't interact directly with the frontend, can be used for crud requests):
  https://polls-app-server-ppm-5a8750ac596d.herokuapp.com/admin/
