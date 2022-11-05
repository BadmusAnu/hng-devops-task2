FROM python:3.9-slim-bullseye


# ENV VIRTUAL_ENV=/opt/venv
# RUN python3 -m venv $VIRTUAL_ENV
# ENV PATH="$VIRTUAL_ENV/bin:$PATH"


RUN apt-get update && apt-get -y install libpq-dev gcc && pip install psycopg2


# Working Directory
WORKDIR /app

# Copy source code to working directory
COPY . /app/

# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install -r requirements.txt

# Expose port 80
EXPOSE 8000

# Run app.py at container launch
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]



