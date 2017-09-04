# Pixel from Lambda
How to easily serve a 1x1 GIF pixel from an Python, lambda-powered endpoint.

## Medium
This project is the companion code for my Medium post on serving a pixel from AWS lambda. Please refer to the Medium blog [post](https://medium.com/@jacopotagliabue/serving-tensorflow-predictions-with-python-and-aws-lambda-facb4ab87ddd#.v01eyg8kh)  for a full explanation on the code structure.

## Deployment
The project comes with a yml file ready to be deployed through [Serverless](https://serverless.com/). After you setup Serverless (don't forget the AWS credentials!), just cd into the prohect folder and launch:

`serverless deploy`

At the end, you will get an OK notification from Serverless and the path to your endpoint.

*Important*: after deployment, remember to add 'image/gif' to "Binary media types" in the API gateway console (see the blog post for a walk-through).