### 0.11.4

- Patch fix docker free space parsing, needed %

### 0.11.3

- Patch fix docker free space parsing

### 0.11.2

- Fix docker info parsing for dockerDiskUtilization

### 0.11.1

- Uses `MemAvailable` from `/proc/meminfo` to determine free memory

### 0.11.0

- Avoids collecting disk utilization information for non-local filesystems

### 0.10.0

- Handles docker disks with > TB of space available

### 0.9.0

- Adds tracking of docker disk space

### 0.8.0

- CWPUT_PERIOD replaces CWPUT_DISABLE_DETAILED. To preserve the behavior of
  CWPUT_DISABLE_DETAILED set CWPUT_PERIOD to `5`.

### 0.7.0

- Adds few seconds jitter around CloudWatch API call
- Set CWPUT_DISABLE_DETAILED to disable detailed monitoring

### 0.6.0

- Submits metrics to CloudWatch in batch
- Checks can no longer set their own namespace

### 0.5.0

- Adds support for awscli 1.5.x.

### 0.4.0

- InstanceId value submitted to CloudWatch is now like
  $INSTANCEID-$STACK_NAME-$EC2_REGION which makes it easier to deal with
  aggregate and non-aggregate metrics within Librato.

### 0.3.0

- Use `AutoScalingGroupName` as the dimension when submitting metrics for an
  instance in an Autoscaling Group.  It is allowed to submit to an ASG that does
  not exist, in case a stack does not have an ASG.

### 0.2.0

- Adds handling for `CWPUT_GROUP` env var to provide value for 2nd metric dimension
- Drops requirement for `autoscaling:DescribeAutoScalingInstances` permission
