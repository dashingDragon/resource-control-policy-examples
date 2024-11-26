## Controls that can be implemented using either SCP or RCP

* Controls that can be enforced using either service control policies (SCPs) or resource control policies (RCPs). 
    * Note that SCPs affect only IAM principals that are managed by accounts that are part of the organization. RCPs impact the effective permissions of principals trying to access resources in a member account with an applicable RCP, regardless of whether the principals belong to the same organizations or not. 




| Included Policy | Rational | 
|------|-------------|
|[Deny users from deleting Amazon S3 Buckets or objects](Deny-users-from-deleting-Amazon-S3-Buckets-or-objects.json) | Restrict users or roles in any affected account from deleting S3 bucket or objects.You can also consider adding this policy as bucket policy on the sensitive buckets.|
|[Deny ACL disablement for all new buckets (bucket owner enforced)](Deny-ACL-disablement-for-all-new-buckets-(bucket-owner-enforced).json)| Require that all new buckets are created with ACLs disabled. Note: When you apply this setting, ACLs are disabled and you automatically own and have full control over all objects in your bucket.|
|[Deny users from modifying S3 Block Public Access (Account-Level)](Deny-users-from-modifying-S3-Block-Public-Access-(Account-Level).json) |Deny users or roles in any affected account from modifying the S3 Block Public Access Account level settings.Note: When you apply block public access settings to an account, the settings apply to all AWS Regions globally.|
|[Prevent S3 buckets from being made public (Bucket level)](Prevent-S3-buckets-from-being-made-public-(Bucket-level).json) |Deny users or roles in any affected account from modifying the S3 Block Public Access bucket level settings.|







