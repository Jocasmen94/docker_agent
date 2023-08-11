# Ado Dockeragent

Self Hosted Agent for Azure Devops

# Set environment variables
echo 'export AZP_URL="https://dev.azure.com/javierjocasmen94/"' >> ~/.bashrc
echo 'export AZP_TOKEN="q7gc4zqftfjhgf3vgeyjtaj3vsccmt3o7uttruvcyylsntcf2viq"' >> ~/.bashrc
echo 'export AZP_AGENT_NAME="my-docker-agent"' >> ~/.bashrc

# Reload the bashrc file to apply the environment variable changes
source ~/.bashrc

# Run the Docker container with the specified environment variables
docker run -e AZP_URL=$AZP_URL -e AZP_TOKEN=$AZP_TOKEN -e AZP_AGENT_NAME=$AZP_AGENT_NAME my-docker-agent:latest

# Modify the token if expired
sed -i '/export AZP_TOKEN="zhaivjr2iuhkxf4wt5iu5u2yi2kz7mrxv7nbw4kbo4dghphvuyga"/d' ~/.bashrc or  sudo nano ~/.bashrc and delete it manually
source ~/.bashrc

test
