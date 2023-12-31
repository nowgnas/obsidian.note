```shell
╷
│ Error: error creating S3 bucket ACL for blooming-blooms-mall: AccessDenied: Access Denied
│       status code: 403, request id: S35AE8YEE5CW78Z3, host id: cC9ouaaFuKJuMcOlNoOnUJ7uUtJnrXxCa421Rw/zd0dPcXQknICsOnLIe4vIYfoUx/DDRVGJ8qo=
│ 
│   with aws_s3_bucket_acl.bb-mall,
│   on s3-mall.tf line 10, in resource "aws_s3_bucket_acl" "bb-mall":
│   10: resource "aws_s3_bucket_acl" "bb-mall" {
│ 
╵

```
https://velog.io/@khyup0629/Terraform-S3-%EB%B2%84%ED%82%B7%EA%B3%BC-CloudFront-%EA%B5%AC%ED%98%84