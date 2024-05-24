# IAM Users and Groups

Identity and Access Management, a global service.

IAM allows us to create users and assign them to groups. 

The root user should ONLY be used to set up your account. 

Users are people within your organization and can be grouped. Example: Developers, Operations, etc.

Groups can only contain users, not other groups. 

Users don't have to belong to groups, but it isn't a best practice. 

Assign groups permissions and users to groups.

Users can belong to multiple groups. 

## Permissions

Users and Groups can be assigned JSON documents called **policies**. 

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

