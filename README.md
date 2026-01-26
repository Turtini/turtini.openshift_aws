# Deploy-an-OpenShift-Cluster-on-AWS-using-Ansible
Deploy an OpenShift Cluster on AWS using Ansible

# 1) Install requirements
ansible-galaxy collection install -r requirements.yml
python3 -m pip install boto3 botocore
brew install awscli  # or your preferred method

# 2) Export AWS creds (or use SSO/role-based auth)
export AWS_PROFILE=myprofile
export AWS_REGION=us-east-1

# 3) Preflight
ansible-playbook -i localhost, playbooks/preflight.yml

# 4) Build foundation
ansible-playbook -i localhost, playbooks/foundation.yml
