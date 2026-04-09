# day-04 - Package Management

## Objectives

- Install and remove packages
- Query packages 
- Practice repo-based management

### Commands:

dnf repolist

dnf install -y httpd

rpm -q httpd

dnf remove -y httpd

rpm -q httpd

dnf install -y httpd

# Broken

- repo unavailable
- package not installed
- package assumed present on other VMs

# Troubleshoot

### Commands

dnf repolist

rpm -q httpd

dnf list installed | grep httpd

# Fixed 

### Commands

dnf install -y httpd

# Validation 

### Commands 

rpm -q httpd
