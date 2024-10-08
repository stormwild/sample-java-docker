FROM azul/zulu-openjdk-alpine:17-latest AS base

# Create a working directory
WORKDIR /app

RUN apk --no-cache add --update \
    bash \
    openssl \
    curl \
    tar \
    ca-certificates

# Copy the Java source file into the container
COPY HelloWorld.java .

# Compile the Java file
RUN javac HelloWorld.java

# Set the command to run the Java application
CMD ["java", "HelloWorld"]