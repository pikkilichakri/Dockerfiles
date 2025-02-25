# Define build-time argument with a default value
ARG version=9

# Use the ARG variable for the base image
FROM almalinux:${version}

# Define additional build-time arguments
ARG course="omnamahashivaya with DevSecOps"
ARG duration="200hrs"

# Set environment variables (persist in the container runtime)
ENV course=$course
ENV duration=$duration
ENV version=$version

# Debug output to verify values
RUN echo "Course: $course, Duration: $duration, Version: $version"

# Keep the container running for testing
CMD ["sleep", "100"]
