Separate subdirectories were created for both Dockerfiles.

Backend: 
- Env variable "REQUEST ORIGIN=http://localhost:5000/" was changed to "REQUEST ORIGIN=http://localhost/".

Frontend:
- Env variable BACKEND_URL=http://localhost/8080/ was removed.

Frontend Dockerfile:
- Command "RUN REACT_APP_BACKEND_URL=http://localhost/8080 npm run build" was changed to "RUN REACT_APP_BACKEND_URL=http://localhost/api/ npm run build