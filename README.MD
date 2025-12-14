---
## Step-1: Create an IAM OIDC provider.

eksctl utils associate-iam-oidc-provider \
    --region us-east-1 \
    --cluster safety-dev \
    --approve
---\

## Step-4: Create an IAM role and Kubernetes ServiceAccount for the LBC and map above policy

eksctl create iamserviceaccount --cluster=safety-dev --name=secret-reader-sa --namespace=safety --attach-policy-arn=arn:aws:iam::996058207546:policy/safetyMYSQLSecretReader --approve
---\






