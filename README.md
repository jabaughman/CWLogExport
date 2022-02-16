Usage Guide
------------------------------

Requirements:
AWS Lambda
Proper permissions for SSM, S3 and Cloudwatch
S3 Bucket to send logs to

* Env variable S3_BUCKET needs to be set. It’s the bucket to export the logs.
* Creates a Cloudwatch Logs Export Task
* It only exports logs from Log Groups that have a tag ExportToS3=true
* It will use the log group name as the prefix folder when exporting
* Saves a checkpoint in SSM so it exports from that timestamp next time
* Only exports if 24 hours have passed from the last checkpoint

