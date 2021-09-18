# CloudFormation-CloudFront-Lab

## Image manager activity with CloudFront

Provided is a cloudformation template to launch a VPC containing two pub and two private subnets. If you had previously launched this same `vpc.yaml` then there's no need to do again.

You will be launching the `imgmgr-cfn.json` and then making changes to it to align with the requirements.

## Acceptance Criteria

Make the necessary modifications to `imgmgr-cfn.json` (your own copy - do not commit to this repo your changes). The following changes are required:

* Remove the ELB
* In place of the ELB we will create an ALB (it'll have just the one clear text HTTP listener)
* ALBs require target groups, we'll add the img server EC2 instances as the target (at the ASG lvl)
* Create a CloudFront distribution
* The cloudfront distro should have the default SSL cert associated with it
* I want all clear text HTTP to be automatically redirected to SSL (at the cloudfront distro)
* for your CF distro have the ALB as the default origin
* No requirements around limiting ALB traffic to the LB (you should be able to hit both the ALB and the CDN independently)
* Post your ALB and CloudFront end points into our teams chat

## Helpfull links/Resources

Cloudformation links:

* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html
* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html
* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html
