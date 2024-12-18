# Docker Compose Release of OpenVPN Access Server

A very simple Docker Compose file to ensure you can just pull this and get up and running with minimum effort.

**Ensure you've set your network appropriately regarding firewall ports.**

## Steps to Get Started

1. **Grab the docker-compose.yml:**
    ```sh
    git clone https://github.com/ramraider2k6/OpenVPN-DCompose.git
    cd OpenVPN-DCompose
    ```

2. **Then start it depending on what release of Docker Compose you have:**
    - For Docker Compose V1:
        ```sh
        docker-compose up -d
        ```
    - For Docker Compose V2 (current version):
        ```sh
        docker compose up -d
        ```

3. **Uncomment line 3 and start Docker Compose:**
    ```sh
    # Edit the docker-compose.yml file and uncomment line 3
    docker-compose up -d
    ```

**Enjoy using TLS 1.3!**

## Finding the Auto-Generated Password to Login

Once the container has started, you'll need to find the auto-generated password to log in.

1. **Get the container ID:**
    ```sh
    docker ps | grep openvpn-as
    ```

2. **Fetch the password (replace `XX` with the container ID):**
    ```sh
    docker logs -f XX | grep pass
    ```

**The username is `openvpn`.**

---

