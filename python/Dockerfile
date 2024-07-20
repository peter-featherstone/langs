FROM python:3.12-alpine as build

RUN apk add --no-cache build-base libffi-dev

RUN pip install uv --no-cache-dir
RUN uv venv

COPY ./requirements.txt requirements.txt
RUN uv pip install --no-cache-dir -r requirements.txt

FROM python:3.12-alpine as runtime

WORKDIR /app
ENV PATH="/.venv/bin:$PATH"

RUN pip install uv --no-cache-dir

COPY --from=build /.venv /.venv
COPY ./ /app

# Add a non root user to run the application.
RUN adduser -SDH -u 1000 app
USER app
