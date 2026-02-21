# NIST 800-53: Configuration Management (CM) Family - AWS Mapping

## CM-2: Baseline Configuration
**Requirement:** Maintain a baseline configuration for the system.
**AWS Technical Evidence:** AWS Config.
**Audit Assertion:** Verify that AWS Config is enabled and recording all resource types. Provide a list of active "Config Rules" that flag deviations from the approved gold image.

## CM-3: Configuration Change Control
**Requirement:** Document and approve changes to the system.
**AWS Technical Evidence:** AWS CloudTrail.
**Audit Assertion:** Provide CloudTrail logs for a 90-day period. Demonstrate that API calls (changes) are tied to an IAM identity and a timestamp, matching authorized change tickets.

## CM-8: Information System Component Inventory
**Requirement:** Maintain an inventory of all system components.
**AWS Technical Evidence:** AWS Systems Manager (SSM) Inventory + AWS Config.
**Audit Assertion:** Export an inventory list of EC2 instances, S3 buckets, and RDS databases. Show that the inventory is updated automatically as resources are created/deleted.
