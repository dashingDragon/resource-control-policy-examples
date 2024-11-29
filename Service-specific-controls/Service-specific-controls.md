## Service specific controls

* Controls that define baseline security requirements or guidelines that are implemented across individual AWS services to ensure a standardized approach to security and compliance.


|Service | Included Policy | Rational | 
|------|-------------|-------------|
|Amazon Simple Storage Service (S3)|[Enforce TLS version](Amazon-S3-bucket-policy-controls:Enforce-TLS-version.json) | Require a minimum TLS version of 1.2 for access to S3 buckets.|
|Amazon Simple Storage Service (S3)|[Deny post and presigned URL requests](Amazon-S3-bucket-policy-controls:Deny-post-and-presigned-URL-requests.json)| Pre-signed URLs are a way to grant temporary access to a private object in your S3 bucket. They allow anyone who possesses the URL to perform the action specified in the URL, such as uploading or downloading a file, without requiring AWS credentials.|
|AWS Key Management Service (KMS)|[Require an AWS Key Management Service key policy limiting creation of AWS KMS grants to AWS services](AWS-KMS-key-controls:Require-an-AWS-Key-Management-Service-key-policy-limiting-creation-of-AWS-KMS-grants-to-AWS-services.json) |Prevent grants from being assigned directly to principals other than AWS service principals to reduce the opportunities for grant misuse.|
|AWS Key Management Service (KMS)|[Require that an AWS Key Management Service asymmetric key with RSA key material used for encryption has a key length greater than 2048 bits](AWS-KMS-key-controls:Require-that-an-AWS-Key-Management-Service-asymmetric-key-with-RSA-key-material-used-for-encryption-has-a-key-length-greater-than-2048-bits.json) |Stronger RSA keys (3072-bit or 4096-bit) are recommended to provide better security.|
|AWS Key Management Service (KMS)|[Require that an AWS KMS key is configured with the bypass policy lockout safety check enabled](AWS-KMS-key-controls:Require-that-an-AWS-KMS-key-is-configured-with-the-bypass-policy-lockout-safety-check-enabled.json) |Deny bypassing the KMS key policy lockout safety check when creating a KMS key or updating its key policy, because bypassing this check increases the risk that a KMS key becomes unmanageable.|
|AWS Key Management Service (KMS)|[Deny the accidental or intentional deletion of a KMS key and only allow specific roles to delete KMS keys.](AWS-KMS-key-controls:Deny-the-accidental-or-intentional-deletion-of-a-KMS-key-and-only-allow-specific-roles-to-delete-KMS-keys.json)|Deny the accidental or intentional deletion of a KMS key and only allow specific roles to delete KMS keys.|











