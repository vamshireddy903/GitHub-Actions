# Git-hub-actions

GitHub Actions is a CI/CD (Continuous Integration and Continuous Deployment) tool built into GitHub that lets you automate workflows directly in your repositories.

# 🔧 Key Features of GitHub Actions:

**Workflow automation**:  Automate building, testing, and deploying your code.

**YAML-based configuration**: Define workflows using .github/workflows/*.yml files.

**Supports containers and VMs**: Run jobs in Docker containers or Ubuntu, Windows, and macOS VMs.

**Matrix builds**: Test across multiple versions of a language or environment.

**Secrets management**: Store sensitive credentials like API keys securely.

**Marketplace actions**: Use pre-built actions from the GitHub Marketplace.

![image](https://github.com/user-attachments/assets/dc3ac90f-b752-4801-accc-6ecaf1eaeb18)

Repository to kick start your journey with GitHub Actions

## Comparing with Jenkins 

### Advantages of GitHub Actions over Jenkins

- Hosting: Jenkins is self-hosted, meaning it requires its own server to run, while GitHub Actions is hosted by GitHub and runs directly in your GitHub repository.

- User interface: Jenkins has a complex and sophisticated user interface, while GitHub Actions has a more streamlined and user-friendly interface that is better suited for simple to moderate automation tasks.

- Cost: Jenkins can be expensive to run and maintain, especially for organizations with large and complex automation needs. GitHub Actions, on the other hand, is free for open-source projects and has a tiered pricing model for private repositories, making it more accessible to smaller organizations and individual developers.

### Advantages of Jenkins over GitHub Actions

- Integration: Jenkins can integrate with a wide range of tools and services, but GitHub Actions is tightly integrated with the GitHub platform, making it easier to automate tasks related to your GitHub workflow.

In conclusion, Jenkins is better suited for complex and large-scale automation tasks, while GitHub Actions is a more cost-effective and user-friendly solution for simple to moderate automation needs.


# Create your own Self-hosted Runners

Step1: Create EC2 and allow HTTP,SSH,HTTPS in both inbound and outbound rules

Step2: Goto github -- settings -- actions -- Runners -- New-self-hosted-runner--Run below commands

![image](https://github.com/user-attachments/assets/654ba81b-6190-4062-9764-c26126143ef1)

# Download

# Create a folder
     
     mkdir actions-runner && cd actions-runnerCopied!# Download the latest runner package
     
    curl -o actions-runner-linux-x64-2.323.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.323.0/actions-runner-linux-x64-2.323.0.tar.gz
    
  # Optional: Validate the hash
    
    echo "0dbc9bf5a58620fc52cb6cc0448abcca964a8d74b5f39773b7afcad9ab691e19  actions-runner-linux-x64-2.323.0.tar.gz" | shasum -a 256 -c
    
  # Extract the installer
    
    tar xzf ./actions-runner-linux-x64-2.323.0.tar.gz

# Configure

# Create the runner and start the configuration experience

     ./config.sh --url https://github.com/vamshireddy903/GitHub-Actions --token BQ2R53URJXYAJUFCL7BI66DIC34UQ# Last step, run it!

# Last step, run it! 
     ./run.sh
# Using your self-hosted runner

# Use this YAML in your workflow file for each job
     runs-on: self-hosted
