AWS_ACCOUNT=$(shell aws sts get-caller-identity --query "Account" --output text)

deploy-common:
	ACCOUNT_ID=$(AWS_ACCOUNT) DEPLOY_ENVIRONMENT=common runway deploy
deploy-dev:
	ACCOUNT_ID=$(AWS_ACCOUNT) DEPLOY_ENVIRONMENT=dev runway deploy
deploy-common-plan:
	ACCOUNT_ID=$(AWS_ACCOUNT) DEPLOY_ENVIRONMENT=common runway plan
