# IAM Users and Groups

Identity and Access Management, a global service.

IAM allows us to create users and assign them to groups. 

The root user should ONLY be used to set up your account. 

Users are people within your organization and can be grouped. Example: Developers, Operations, etc.

Groups can only contain users, not other groups. 

Users don't have to belong to groups, but it isn't a best practice. 

Assign groups permissions and users to groups.

Users can belong to multiple groups. 

## A Global Service

IAM settings are GLOBAL. Once you set them, they are available in ALL regions. You can see this when you drop into the IAM Console. In the drop-down menu for regions, you will see the word "Global" for these types of services. 

## Permissions

Users and Groups can be assigned JSON documents called **policies**, which looks like the example below.

```json

{
    "Version":"2012-10-17",
    "Statement":[
        {
            "Effect":"Allow",
            "Action":"ec2:Describe",
            "Resource":"*"
        },
        {
            "Effect":"Allow",
            "Action":"elasticeloadbalancing:Describe",
            "Resource":"*"
        },
        {
            "Effect":"Allow",
            "Action":[
                "cloudwatch:ListMetrics",
                "cloudwatch:GetMetricStatistics",
                "cloudwatch:Describe"
            ],
            "Resource":"*"
        }
    ]
}
```

In AWS you should provide the principle of least privledge. That might be in the test.

## Account Alias

It is possible to create an alias for the root account, which changes and simplifies the console login URL.

Example: Joe Bob has the accont number of 876xxxx and wants to simplify that. He adds an alias for his root account of joebob and now when he goes to the AWS console he can enter that alias instead of his account number, and then login as his admin user. 

