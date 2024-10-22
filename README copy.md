# Server Configuration Workflow

This repository contains the necessary files and instructions to set up and configure servers using Ansible.

## Files

- `ansible_setup_serwer.yaml`: Ansible playbook for initial server setup.
- `server_setup.yml`: Ansible playbook for detailed server configuration.

## Prerequisites

- Ansible installed on your local machine.
- SSH access to the target servers.

## Usage

1. **Clone the repository:**
  ```sh
  git clone https://github.com/yourusername/ServerConfigInternal.git
  cd ServerConfigInternal
  ```

2. **Run the initial server setup:**
  ```sh
  ansible-playbook ansible_setup_serwer.yaml
  ```

3. **Run the detailed server configuration:**
  ```sh
  ansible-playbook server_setup.yml
  ```

## Contributing

Feel free to submit issues or pull requests if you find any bugs or have suggestions for improvements.

## License

This project is licensed under the MIT License.

export ADMIN_USER=admin
export ADMIN_PASSWORD=123456
export ADMIN_EMAIL=test@test.com
export POSTGRES_USER=postgres
export POSTGRES_PASSWORD=123456
export POSTGRES_DB=postgres

export AWS_ACCESS_KEY_ID=
export AWS_SECRET_ACCESS_KEY=
export AWS_REGION=eu-central-1
export S3_BUCKET_NAME=packeton-spear

ansible-playbook -i playbooks/host.ini playbooks/server_setup.yml --private-key Ansible_test_aws.pem -u ubuntu
