# S3
S3 important Commands

### Create Bucket
aws s3 mb s3://tgsbucket --region us-west-2  //region is optional

#### Remove Bucket
aws s3 rb s3://tgsbucket --force

#### List files in bucket

aws s3 ls
aws s3 ls s3://tgsbucket
aws s3 ls s3://tgsbucket --recursive
aws s3 ls s3://tgsbucket --recursive  --human-readable --summarize


# s3 cp commands
aws s3 cp getdata.php s3://tgsbucket
aws s3 cp /local/dir/data s3://tgsbucket --recursive
aws s3 cp s3://tgsbucket/getdata.php /local/dir/data
aws s3 cp s3://tgsbucket/ /local/dir/data --recursive
aws s3 cp s3://tgsbucket/init.xml s3://backup-bucket
aws s3 cp s3://tgsbucket s3://backup-bucket --recursive

# s3 mv commands
aws s3 mv source.json s3://tgsbucket
aws s3 mv s3://tgsbucket/getdata.php /home/project
aws s3 mv s3://tgsbucket/source.json s3://backup-bucket
aws s3 mv /local/dir/data s3://tgsbucket/data --recursive
aws s3 mv s3://tgsbucket s3://backup-bucket --recursive


# s3 rm commands
aws s3 rm s3://tgsbucket/queries.txt
aws s3 rm s3://tgsbucket --recursive

# s3 sync commands
aws s3 sync backup s3://tgsbucket/myfolder
aws s3 sync s3://tgsbucket/backup /tmp/backup
aws s3 sync s3://tgsbucket s3://backup-bucket
