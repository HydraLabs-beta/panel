<p align="center">
    <img src="https://raw.githubusercontent.com/HydraLabs-beta/sedar/main/hydrapanel2.png" alt="HydraPanel Logo">
</p>
<h2> HydraPanel is an open source panel for managing your game servers, applications and more built with modern technologies such as Node.js, Docker and Express - made to work with our HydraDaemon software.</h2>

## Installation
### Picking a Server OS

HydraPanel runs on a wide range of operating systems, so pick whichever you are most comfortable using.

| Operating System | Version |     Supported      | Notes                                                       |
|------------------|---------|:------------------:|-------------------------------------------------------------|
| **Ubuntu**       | 24.04   | ✅ | Documentation written assuming Ubuntu 24.04 as the OS. |
|                  | 22.04   | ✅ |                                                             |
| **CentOS**       | 7       | ✅ | Extra repos are required.                                   |
|                  | 8       | ✅ | Note that CentOS 8 is EOL. Use Rocky or Alma Linux.         |
| **Debian**       | 11      | ✅ |                                                             |
|                  | 12      | ✅ |                                                             |
| **Windows**      | 11      | ⚠️ | May have issues due to Windows' firewall.                   |
|                  | 10      | ⚠️ |                                                             |
| **macOS**        | 10.15+  | ⚠️ |                                                             |

## Dependencies

* Node.js `v20` and higher (Nodejs `v20` recommended).

### Example Dependency Installation

The commands below are simply an example of how you might install these dependencies on Ubuntu 24.04. Please consult with your
operating system's package manager to determine the correct packages to install.

```sh
# Ubuntu/Debian
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_16.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

sudo apt update
sudo apt install -y nodejs git
```

## Installation

The following commands will download the Hydra Panel into /etc/hydra and use npm to install the required packages:

``` bash
cd /etc
git clone https://github.com/hydren-dev/HydraPanel
mv HydraPanel hydra
cd hydra
npm install
```

### Seed & Create a User

You'll then need to create an administrative user so that you can log into the panel. To do so, run the command below.

``` bash
npm run seed
npm run createUser
```

### Setup Complete

All you need to do now is start HydraPanel:
``` bash
node .
```

Your Panel will now be accessible from port 3001 (unless you changed it in `config.json`).

# Credits
- Skyport (EOL)
- SRYDEN (https://sryden.com)
