# Steps for Practical on EBS backend 

## Prerequisite:
1. EKS cluster/ Cluster inside AWS
2. Authorization to use EKS , EBS

## Steps to configure Cluster to use EBS
- Steps1: Permission to access EBS From Node
    NodeGroup -> NodeRole (amazonEBSCSIDriverpolicy)
- Step2: Create NodeGroup
- Step3: Add-on EBS CSI DRIVER using console
- step4: Check EBS-CSI-DRIVER installed
    ` kubectl get pods -n kube-system | grep ebs `

## Steps to use EBS volume with PV
- Step1: Create EBS Volume using Console
- step2: Format volume with FileSytsyem EXT4
    - laumch temp ec2 instance in same AZ as volume
    - attach volume to temp instance
    - format using ext4 : ` mkfs -t ext4 /dev/xvdf`
    - detach from temp instance
- step3: Create PV
- step4: create PVC
- step5: Create POD