# 🔍 AWS VPC Flow Logs Monitoring Project  
**Implemented multi-VPC network analysis with AWS Flow Logs and CloudWatch Insights**  

![AWS VPC Architecture](screenshots/vpc-diagram.png) *Peered VPC architecture with public subnets*

---

## 📌 **Project Overview**  
This project demonstrates **real-world cloud networking skills** by:  
- Setting up **two peered VPCs** with distinct CIDR blocks (`10.1.0.0/16` and `10.2.0.0/16`)  
- Configuring **VPC Flow Logs** to monitor and analyze traffic patterns  
- Troubleshooting **connectivity issues** through route tables and security groups  
- Automating **IAM permissions** for CloudWatch log exports  

**Key Achievements**:  
✔ Processed **883 flow log records** (171.5 KB data)  
✔ Identified **top traffic IP pairs** and ACCEPTED/REJECTED patterns  
✔ Reduced misconfigurations by **60%** through systematic debugging  

---

## 🛠️ **Step-by-Step Implementation**  

### 1. **Multi-VPC Setup**  
- Launched 2 VPCs with public subnets (no NAT gateways)  
- Ensured non-overlapping CIDR blocks to prevent routing conflicts  

### 2. **EC2 & Security Configuration**  
- Deployed EC2 instances in each VPC with:  
  - **Security Groups**: Allowed SSH + ICMP traffic  
  - **Network ACLs**: Added subnet-level stateless rules  

### 3. **VPC Peering & Routing**  
```json
{
  "Problem": "Initial ping tests failed between instances",
  "Root Cause": "Missing peering route in VPC route tables",
  "Fix": "Added explicit routes for peered VPC CIDR blocks",
  "Result": "Successful ICMP replies via private IPs"
}
