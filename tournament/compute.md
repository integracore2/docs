# Numerai Compute

## Introduction

Compute is a framework to help you automate your weekly submission workflow __with your own infrastructure.

Use the [numerai-cli](https://github.com/numerai/numerai-cli) to provision your infrastructure, and deploy your pre-trained model as a server that listens for new tournament data, runs your model and uploads the predictions back to Numerai.

![](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LhIINlU0vnTY9ulNmAH%2F-LjcTM9mF7HKAM9kD3qm%2F-LjcTYRaegP4jfdnrWGL%2Fcompute_architecture.png?alt=media&token=da7df4e6-69c3-47bd-8daa-217494464077)

## Quick start

```text
pip3 install numerai-cli

mkdir example-numerai
cd example-numerai

# set up your compute node in AWS
numerai setup

# copy a python example model
numerai docker copy-example

# build the docker container and deploys it to AWS
numerai docker deploy

# trigger your compute node in AWS
numerai compute test-webhook

# watch the logs of the running compute node from AWS
numerai compute logs -f
```

## Help <a id="getting-started"></a>

Follow our step by step [tutorial](https://docs.numer.ai/help/compute-tutorial) or watch the video on [YouTube](https://www.youtube.com/watch?v=YFgXMpQszpM).

Ask for help in the [compute rocketchat channel](https://community.numer.ai/channel/compute).



