FROM python:3.10-slim-buster

WORKDIR /backend-flask

FRONTEND_URL="*" BACKEND_URL="*" docker run --rm -p 4567:4567 -it backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
#python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

#corrent URL: https://4567-cloudnative-awsbootcamp-sqv1j5j6q45.ws-us87.gitpod.io/api/activities/home

#Use the unset command to delete the variables during program execution.
# It can remove both functions and shell variables. Using the unset command, you can unset values and attributes of shell variables and functions