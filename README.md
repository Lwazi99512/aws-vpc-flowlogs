# 🔍 AWS VPC Flow Logs Monitoring  
*Analyzing network traffic between peered VPCs*  

## 📌 Key Achievements  
- **Troubleshooted ICMP connectivity** via route table updates  
- **Processed 883 Flow Log records** (171.5 KB data)  
- **Identified top traffic IP pairs** using CloudWatch Insights  

## 🛠️ Step-by-Step Implementation  
### 1. Multi-VPC Setup  
- Launched 2 VPCs (`10.1.0.0/16` and `10.2.0.0/16`)  
- Configured public subnets (no NAT gateways)  

### 2. Peering & Routing  
```json
{
  "Problem": "Initial ping tests failed",
  "Fix": "Added peering route to VPC route tables",
  "Result": "Successful ICMP replies via private IPs"
}
