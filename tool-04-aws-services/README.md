
## S3: Upload and Download Files

Great for storing anything such as images, backups, and logs.

```bash
aws s3 cp file.txt s3://my-bucket/
aws s3 cp s3://my-bucket/file.txt ./
```

---

## Lambda: Hello World (No Server)

Let AWS run your code without managing servers.

```python
def lambda_handler(event, context):
    return {'statusCode': 200, 'body': 'Hello from Lambda!'}
```

Create from AWS Console → Paste → Deploy → Test.

---

## CloudWatch: Monitor EC2 CPU

Tracks EC2 metrics such as CPU utilization. You can set alarms to get notified of performance issues.

---

## CloudFormation: Infrastructure as Code to Deploy EC2

Write your infrastructure as YAML. AWS builds it automatically.

```yaml
Resources:
  MyEC2:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      ImageId: ami-0abcd1234
      KeyName: my-key-pair
```

---

## ECR: Push Docker Image

AWS ECR acts as a private Docker image registry. Push your images there.

```bash
docker tag myapp <ECR_URL>/myapp:latest
docker push <ECR_URL>/myapp:latest
```

---

## CloudFront: CDN for S3 Website

CloudFront caches your S3-hosted static website globally for better performance.

Steps:

1. Upload files to S3
2. Enable static hosting
3. Create CloudFront distribution with S3 as origin
4. Access the site via CloudFront URL

---

