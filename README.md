Terraform project structure. 

```
/
├── environments/               # Separate configurations by environment
│   ├── dev/                    # Development environment configurations
│   │   ├── main.tf             # Define core resources for dev
│   │   ├── variables.tf        # Declare dev-specific variables
│   │   ├── provider.tf         # Configure provider for dev
│   │   ├── outputs.tf          # Output values for dev resources
│   │   └── dev.tfvars          # Set dev-specific variable values
│   │
│   ├── staging/                # Staging environment configurations
│   │   └── ... (same structure as 'dev')
│   │
│   └── prod/                   # Production environment configurations
│       └── ... (same structure as 'dev' and 'staging')
│
├── modules/                    # Centralized reusable Terraform modules
│   ├── network/                # Network module (e.g., VPC)
│   │   ├── main.tf             # Define VPC, subnets, etc.
│   │   ├── variables.tf        # Input variables for VPC settings
│   │   └── outputs.tf          # Outputs for VPC, subnet IDs
│   │
│   ├── compute/                # Compute module (e.g., EC2 instances)
│   │   ├── main.tf             # Define compute configurations
│   │   ├── variables.tf        # Input variables for instance settings
│   │   └── outputs.tf          # Outputs for instance IPs and IDs
│   │
│   └── data/                   # Data module (e.g., S3 bucket)
│       ├── main.tf             # Define data configurations
│       ├── variables.tf        # Input variables for bucket settings
│       └── outputs.tf          # Outputs for bucket name and ARN
```
