# MLOps Zoomcamp Setup

- Create an instance
- Create a key to ssh into the instance
- Connect the instance `ssh -i ~/.ssh/<your key name>.pem ubuntu@<your instance ip>`
- We can edit ssh config file `nano ~/.ssh/config`

```yaml
Host apollo
        HostName 3.69.180.43
        User ubuntu
        IdentityFile ~/.ssh/apollo.pem
        StrictHostKeyChecking no
```

This way we don’t have type everything next time. Just type `ssh apollo`.

- Update package manager `sudo apt update`
- Get docker from package manager `sudo apt install docker.io`
- Find the latest docker-compose from [github](https://github.com/docker/compose/releases/tag/v2.5.1) page
- Download it to a seperate folder `wget https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-x86_64 -O docker-compose`
- Make docker-compose executable `chmod +x docker-compose`
- Modify PATH. To do that edit ~/.bashrc `nano ~/.bashrc` and add this line

```bash
export PATH="${HOME}/soft:${PATH}”
export PATH="${HOME}/soft:${PATH}"
```

- Refresh bashrc `source ~/.bashrc`

You can check it by typing `docker-compose` from any location. Or you can ask which docker-compose it will use `which docker-compose`

- Add your current user to docker group because of the permission. Only docker user group can run docker by default. `sudo usermod -aG docker $USER`
- Now you can run docker `docker run hello-world`

- Clone the repo `git clone https://github.com/DataTalksClub/mlops-zoomcamp.git`

Now switch to VSCode, install “Remote-SSH” extension. After it is installed, on the bottom left, click the icon looks like ><. Connect the host and you will see the host we’ve defined above. And open the directory where we cloned the git repo.

### Jupyter Notebooks

- Start a jupyter notebook inside the instance. Now it is serving the notebook.
- Go to VSCode and forward a port. It is done on Ports tab in terminal window in VSCode.
