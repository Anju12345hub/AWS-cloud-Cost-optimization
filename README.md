# AWS Cloud Cost Optimization - Identifying Stale Resources
Identifying Stale EBS Snapshots.
# Description:
The AWS Lambda function in this example helps optimize cloud costs by identifying and deleting stale EBS (Elastic Block Store) snapshots that are no longer associated with any active EC2 (Elastic Compute Cloud) instance.
It does this by fetching all EBS snapshots owned by the account, as well as a list of active EC2 instances (both running and stopped).
For each snapshot, it verifies if the associated EBS volume is not connected to any active instance. If a snapshot is found to be stale, it is deleted, thereby reducing storage costs and improving resource efficiency in the AWS cloud environment.
