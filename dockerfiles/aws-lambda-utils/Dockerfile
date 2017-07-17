FROM liangrog/aws-lambda-ami-go:1.8.3

USER root

# Get boto3
RUN pip uninstall -y botocore
RUN pip install -U boto3

# Insatll lmdo
RUN pip install --no-cache-dir lmdo
