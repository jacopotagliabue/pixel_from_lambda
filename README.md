# Pixel from Lambda
How to easily serve a 1x1 GIF pixel from an Python, lambda-powered endpoint.

## Medium Post
This project is the companion code for my Medium post on serving a pixel from AWS lambda. Please refer to the Medium blog [post](https://medium.com/@jacopotagliabue/serving-tensorflow-predictions-with-python-and-aws-lambda-facb4ab87ddd#.v01eyg8kh)  for a full explanation on the code structure.

## Deployment
The project comes with a yml file ready to be deployed through [Serverless](https://serverless.com/). After you setup Serverless (don't forget the AWS credentials!), just cd into the prohect folder and launch:

`serverless deploy`

At the end, you will get an OK notification from Serverless and the path to your endpoint.

**Important**: after deployment, remember to add 'image/gif' to "Binary media types" in the API gateway console (see the blog post for a walk-through).

## Tests
From the terminal, run the following to download the pixel:

`curl -H "Accept:image/gif" https://{LAMBDA_URL}/{LAMBDA_ENV}/pixel > pixel.gif`

where {LAMBDA_URL} is the URL returned by the Serverless deployment and {LAMBDA_ENV} is specified in the yml file.
To test the full browser experience, modify the path in the image tag in *hello_pixel.html* and open the page.


 

 