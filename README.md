# AWS Cloud Cost Optimization - Identifying Stale Resources
Identifying Stale EBS Snapshots.
# Description:
The AWS Lambda function in this example helps optimize cloud costs by identifying and deleting stale EBS (Elastic Block Store) snapshots that are no longer associated with any active EC2 (Elastic Compute Cloud) instance.
It does this by fetching all EBS snapshots owned by the account, as well as a list of active EC2 instances (both running and stopped).
For each snapshot, it verifies if the associated EBS volume is not connected to any active instance. If a snapshot is found to be stale, it is deleted, thereby reducing storage costs and improving resource efficiency in the AWS cloud environment.

# Steps:


Step 1: Create an EC2 instance; by default, it generates a volume.

Step 2: Navigate to snapshots and create a snapshot (for example, named cost-optimization-ebs-snap).

Step 3:Develop a Lambda function (ebs-stale-snapshot.py) with the objective of deleting the snapshot if its volume is not associated with any active instance.

Step 4: Prior to executing the code, add the necessary permissions. Create a policy, choose the EC2 service, and allow actions such as delete snapshot, describe snapshot, describe volume, and describe instance. Name the policy (cost-optimization-ebs).

step 5:go to configuration -->role--> add permission-->selet the policy(cost-optimization-ebs)

Now, proceed to test the code.

