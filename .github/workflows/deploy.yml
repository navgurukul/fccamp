name: Deploy on Push or PR Merge

on:
  push:
    branches:
      - dev
      - main
  pull_request:
    types:
      - closed # This triggers when a PR is merged or closed

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Setup SSH
      uses: webfactory/ssh-agent@v0.5.3
      with:
        ssh-private-key: ${{ secrets.SSH_PRIVATE_KEY }}

    - name: Run deployment script based on branch
      run: |
        ssh -o StrictHostKeyChecking=no ubuntu@hi.navgurukul.org << 'EOF'
        
        if [ "${{ github.ref }}" == "refs/heads/dev" ]; then
          ./deploy-fcc-dev.sh    # Run this script for dev branch
        elif [ "${{ github.ref }}" == "refs/heads/main" ]; then
          ./deploy-fcc-main.sh   # Run this script for main branch
        fi
        EOF
      env:
        SSH_PRIVATE_KEY: ${{ secrets.SSH_PRIVATE_KEY }}
        SSH_USER: ubuntu
        SSH_HOST: hi.navgurukul.org
