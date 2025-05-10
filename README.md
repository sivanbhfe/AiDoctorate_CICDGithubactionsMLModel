    # Setup Virtual Environment

```python
conda create -n fastapi-env python=3.10
conda activate fastapi-env
pip install -r requirements.txt
```

# Running the server
`uvicorn main:app --reload`
# `uvicorn main:my_first_api --reload`

The command `uvicorn main:app` refers to:
- main: the file main.py (the Python "module").
- app: the object created inside of main.py with the line app = FastAPI().
- --reload: make the server restart after code changes. Only use for development.


```json
Yes

```

```bash
curl -X 'POST' \
  'http://127.0.0.1:8005/predict' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "Dependents": 2,
  "Education": "Graduate",
  "Self_Employed": "Yes",
  "TotalIncome": 110,
  "LoanAmount": 220,
  "Loan_Amount_Term": 220,
  "Credit_History": 220,
  "Residential_Assets_Value": 110,
  "Commercial_Assets_Value": 110,
  "Luxury_Assets_Value": 110,
  "Bank_Asset_Value": 110
}'

```

# ci-cd-python - Commands to install Docker on EC2 
- Ensure port 80 is available
```

# MUST STEPS create ECR with name: my-mlapp
sudo yum update -y
sudo amazon-linux-extras install docker -y
sudo service docker start
sudo systemctl start docker
sudo service docker status
sudo groupadd docker
sudo usermod -a -G docker ec2-user
newgrp docker
docker —-version

# MUST STEP create ECR with name: my-mlapp
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 866824485776.dkr.ecr.us-east-1.amazonaws.com
```

# GIT ACTIONS SECRETS
AWS_ACCESS_KEY_ID - Create a Key pair in your IAM User (sivabalan in AWS console - but this will be displayed as ec2-user in AWS CLI)
AWS_SECRET_ACCESS_KEY - Corresponding Secret key
AWS_ACCOUNT_ID - You AWS account ID
AWS_REGION - Your AWS region
EC2_HOST - public address ipv4 DNS from EC2 instance
EC2_SSH_KEY - Pre-empt to all SSH Key pair to connect to EC2 instance
EC2_USERNAME - (username - sivabalan) but used as ec2-server (default in aws cli)
