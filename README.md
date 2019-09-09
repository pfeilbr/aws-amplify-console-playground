# aws-amplify-console-playground

lean [AWS Amplify Console](https://docs.aws.amazon.com/amplify/latest/userguide/welcome.html)

> AWS Amplify Console is a continuous delivery and hosting service for modern web applications. The AWS Amplify Console simplifies the deployment of your application front end and backend. Connect to your code repository and your front end and backend are deployed in a single workflow, on every code commit.

Build setting are defined in [`amplify.yml`](amplify.yml).  See [Configuring Build Settings](https://docs.aws.amazon.com/amplify/latest/userguide/build-settings.html) for YML Specification Syntax.

---

set amplify service role.  codebuild env will assume this role and commands will execute in this context.
![](https://www.evernote.com/l/AAGKI4wgfUZB7YtWVDmqTmfg9YEzYSa4L38B/image.png)

showing assumed role in codebuild env
![](https://www.evernote.com/l/AAFxwKOPnvJLYb7DpmMr5vF7wLiU-xHSxUQB/image.png)

Update SAM deploy bucket policy to allow amplify service (`amplify.amazonaws.com`) to read/write to bucket.
![](https://www.evernote.com/l/AAHR9UMPba1ExLJ3iyLjgFUXFRWfOZhHP-0B/image.png)