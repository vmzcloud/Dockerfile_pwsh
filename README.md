https://docs.microsoft.com/en-us/powershell/scripting/install/install-centos?view=powershell-7.1

    # Register the Microsoft RedHat repository
    curl https://packages.microsoft.com/config/rhel/8/prod.repo | sudo tee /etc/yum.repos.d/microsoft.repo

    # Install PowerShell
    sudo yum install -y powershell

    # Start PowerShell
    pwsh
    
## Docker Build

    docker build -f Dockerfile_pwsh_centos7 -t vmzcloud/pwsh:centos7 .
    
## Docker Run

    docker run --rm -it vmzcloud/pwsh:centos7 pwsh

## Powershell Command

### Check PowerShell Version

    PS /> $PSVersionTable.PSVersion

    Major  Minor  Patch  PreReleaseLabel BuildLabel
    -----  -----  -----  --------------- ----------
    7      2      1                      
