# 🛠 Tool 01: Ansible

## 📌 What is Ansible?
Ansible is an open-source configuration management tool that automates software provisioning, configuration, and application deployment using YAML playbooks.


## Goal of This Demo

Install **Nginx** on the local machine using an Ansible playbook.


## Files in This Demo

| File              | Purpose                            |
|-------------------|------------------------------------|
| `hosts.ini`       | Inventory file (targets localhost) |
| `install-nginx.yml` | Playbook to install Nginx         |


## 💻 Run Instructions

### ✅ 1. Install Ansible

sudo apt update
sudo apt install ansible -y

### ✅ 2. Run the Playbook
ansible-playbook -i hosts.ini install-nginx.yml

## summary
| Variable      | Use Case Example               |
| ------------- | ------------------------------ |
| `hosts`       | Target machine(s) for playbook |
| `become`      | Run with sudo                  |
| `vars`        | Define re-usable values        |
| `vars_files`  | Load external variable files   |
| `vars_prompt` | Get user input dynamically     |
| `tasks`       | List of actions                |
| `handlers`    | Trigger only when notified     |
| `register`    | Save task output               |
| `when`        | Conditional execution          |
| `tags`        | Run specific parts of playbook |
| `with_items`  | Loop through list              |
| `delegate_to` | Run on another host            |
| `environment` | Set environment variables      |



