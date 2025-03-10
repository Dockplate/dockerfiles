FROM python:3.9-slim

# Build arguments
ARG VCS_REF
ARG BUILD_DATE

# Adding Labels
LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date="${BUILD_DATE}"
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref="${VCS_REF}"

# Copy and set up working directory
COPY ./src /src
WORKDIR /src

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Execution
CMD ["python", "hello_python.py"]