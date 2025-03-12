FROM langflowai/langflow:latest

# https://github.com/langflow-ai/langflow/issues/4594

# Install pip in the virtual environment
RUN /app/.venv/bin/python -m ensurepip --upgrade

# Install the dependencies
RUN /app/.venv/bin/python -m pip install jsonpath-ng

# Set the environment variable to use the virtual environment’s Python by default
ENV PATH="/app/.venv/bin:$PATH"

CMD ["python", "-m", "langflow", "run", "--host", "0.0.0.0", "--port", "7860"]
