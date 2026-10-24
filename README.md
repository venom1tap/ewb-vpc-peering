# AWS VPC Peering - EWB Cloud Labs Project 01

**Name:** Aryan Rao  **Batch:** Batch 1  **Region:** ap-south-1 (Mumbai)  **Date:** 24 October 2026

Two private VPCs connected with VPC peering, built with the AWS Console. One public bastion host in VPC A is used for SSH (ProxyJump). No NAT gateway.

| Resource | CIDR / IP |
|---|---|
| ewb-vpc-a | 10.10.0.0/16 |
| ewb-a-public / ewb-a-private | 10.10.1.0/24 / 10.10.2.0/24 |
| ewb-vpc-b / ewb-b-private | 10.20.0.0/16 / 10.20.1.0/24 |
| ewb-bastion / ewb-app-a / ewb-app-b | 10.10.1.10 / 10.10.2.10 / 10.20.1.10 |
| Peering | ewb-a-b-peer (pcx-0872ea58430aa0767), Active |

## Results
- Baseline before peering: 100% packet loss
- After peering and routes: App-A to App-B and App-B to App-A, 0% packet loss
- SSH to App-B through the bastion works
- App-A and App-B have no public IPv4
- Controlled failure: removed ICMP rule, ping failed; restored rule, ping recovered
- Cleanup done, only default VPC left

## Files
- `Aryan_Rao_EWB_VPC_Peering_Final.pdf`: full report
- `screenshots/`: numbered evidence screenshots (01 to 29)
