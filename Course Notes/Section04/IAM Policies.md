# IAM Policies

## Inheritance

Users inherit their policies from their groups. Users can have multiple groups and the policies are additive.

## Policy Structure

Policies are structured in JSON documents.

```json
{
    "Version":"2012-10-17",
    "Id":"S3-Account-Permissions",
    "Statement":[
        {
            "Sid":"1",
            "Effect":"Allow",
            "Principal":{
                "AWS":["arn:aws:iam::xxxx:root"]
            },
            "Action":[
                "s3:GetObject",
                "s3:PutObject"
            ],
            "Resource":["arn:aws:s3:::bucketName/*"]
        }
    ]
}
```

## Defintions

**Version**: The policy language version. Always include "2012-10-17"

**Id**: An identifier for the policy. User selected. Optional.

**Statement**: One or more individual statements (required)

### Statements consist of

* Sid: An identifier for the statement (optional)
* Effect: Either Allow or Deny
* Principal: account, user, or role that this policy applies to.
* Action: A list of actions this policy allows or denies.
* Resource: A list of resources this action applies to.
* Condition: Conditions for when this policy is in effect (optional, no example)