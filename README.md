# Health Check Tool

Welcome! If you’re here, you’re either exploring automation projects or checking out my profile for a potential collaboration. This project is designed to showcase a simple yet effective automated health check tool using Ansible and Jenkins. It periodically monitors server health, generates reports, and sends alerts in case of any issues.

## Features
- Automated health checks for CPU, memory, and disk usage.
- Scheduled execution using Jenkins.
- Generates and archives health check reports.
- Sends email alerts if any health checks fail.

## Project Structure

```
health-check-tool/
├── health_check.yml        # Ansible playbook for performing health checks
├── hosts.ini               # Inventory file with server details
├── screenshots/            # Contains screenshots for documentation
│   ├── jenkins_setup.png   # Screenshot of Jenkins job setup
│   ├── console_output.png  # Screenshot of console output in Jenkins
│   ├── health_report.png   # Screenshot of sample health report
└── README.md               # Project documentation (you are here!)
```

## Setup Instructions

1. **Clone this repository.**
   ```bash
   git clone https://github.com/your-username/health-check-tool.git
   ```

2. **Configure Jenkins to pull from this repository and run the `health_check.yml` playbook.**
   - Set up a Jenkins job that runs the Ansible playbook as a build step.
   - Ensure that Jenkins has the required permissions to execute Ansible.

3. **Schedule Jenkins to run the job daily and configure email notifications.**
   - In the Jenkins job, set up a build trigger to schedule the job to run daily.
   - Configure email notifications in Jenkins to alert in case of a failure.

## Example Output
Here’s an example of the health report output generated by Ansible:

### Disk Usage:
```plaintext
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           566M  1.6M  565M   1% /run
/dev/sda2        25G   18G  6.0G  75% /
tmpfs           2.8G  128K  2.8G   1% /dev/shm
tmpfs           5.0M  8.0K  5.0M   1% /run/lock
tmpfs           566M  132K  566M   1% /run/user/1000
```

### CPU Usage:
```plaintext
cpu  113555 586 168385 3319796 5176 0 30562 0 0 0
```

### Memory Usage:
```plaintext
               total        used        free      shared  buff/cache   available
Mem:           5.5Gi       3.8Gi       160Mi        86Mi       1.9Gi       1.8Gi
Swap:          4.0Gi       4.0Mi       4.0Gi
```

## Screenshots


Below are screenshots that demonstrate the Health Check Tool in action.

1. **Jenkins Job Setup Screenshot**
   This screenshot shows the configuration of the Health Check Job in Jenkins. Here, we set up the job to run the Ansible playbook and monitor system health.

![image](https://github.com/user-attachments/assets/df24b4ef-1347-4569-93db-5f15071c3517)


2. **Console Output in Jenkins**
   After executing the Health Check Job, Jenkins provides a detailed console output. This output shows the steps of the Ansible playbook as it checks CPU, memory, and disk usage on the target server.

![image](https://github.com/user-attachments/assets/31122827-aac0-4ab2-b705-f80055492d6f)

3. **Sample Health Report**
   This is an example of the health report generated by the tool. The report includes CPU, memory, and disk usage metrics, helping identify any potential issues.

![image](https://github.com/user-attachments/assets/99502301-57c4-45da-aaa5-d7267f97a4dc)






