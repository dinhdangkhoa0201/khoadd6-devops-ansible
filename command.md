ansible-playbook main.yml -i inventory --private-key ~/.ssh/khoadd6.devops.ec2.pem

aws cloudformation deploy \
--template-file cloudfront.yml \
--stack-name production-distro \
--parameter-overrides PipelineID="khoadd6-devops-bucket"
