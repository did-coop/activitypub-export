## Deployments

### Deploy to Staging Server

To deploy Hollo to the staging server, follow these steps:

1. **Generate an SSH Key**:

   - Generate an SSH key on your local machine:
     ```bash
     ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
     ```
   - Add the generated public key (`~/.ssh/id_rsa.pub`) to the server's authorized keys.

2. **Connect to the Server**:

   - Use SSH to connect to the server:
     ```bash
     ssh username@208.113.133.153
     ```

3. **Run the Deployment Script**:
   - Run the deployment script:
     ```bash
     /opt/deploy_hollo.sh
     ```
   - [Optional] in case you want to deploy a specific branch:
     ```bash
     /opt/deploy_hollo.sh branch_name
     ```
   - The script will:
     - Pull the latest changes from the repository.
     - Restart the application.
