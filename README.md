# LW-project
MP3/MP4 content summary generator using GPT model and sending it using SMTP.
I have created a microservice-architecture based MP3/MP4 content summary generator using GPT model and sending the summary by SMTP. In this we can upload any file of format MP3/MP4 or text through a API-Gateway or directly in S3. Then that will initiate the lambda function and it will transfer the content to transcribe service and transcribe will return the text content from the file. And it will be transfered to another S3 bucket and it will initiate another lambda function will use GPT model to generate summary of the content and after this, it will send email to the concerned person using sns service.
After all of this users will get the short and exact summary from the content which we have uploaded.
We are using lambda service, API-Gateway, SNS , IAM, Transcribe, GPT etc.
