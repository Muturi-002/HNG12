# Stage 0
This is the first stage of the internship at HNG Tech cohort 12.
## Task
- Use a fresh Ubuntu instance.
- Install NGINX web server and it must be running smoothly.
- Custom the server to serve a custom HTML page as the default page (/var/www/html/index.html) with the message:
    “Welcome to DevOps Stage 0 - [Your Name]/[SlackName]”
- Only allow incoming traffic to port 80.

Cloud platform used: Oracle Cloud Infrastructure (OCI)
## Steps
1. In the cloud console, create an instance with the necessary requirements (virtual network, image and shape). Ensure you tag the instance and the related components. Download the ssh keys in a local repository.
2. Go to the working directory using an IDE, and in the terminal, ssh the instance using its IP address and the SSH public key.
3. Configure the firewall using the following commands:
    - `sudo ufw enable`
    - `sudo ufw allow http`
    - `sudo ufw status` or `sudo ufw status verbose` - confirms that incoming traffic is allowed through port 80.
4. Install the NGINX server using the following command: `sudo apt install nginx`. Run the command `sudo systemctl enable nginx` followed by `sudo systemctl status nginx` to confirm that it is active.
5. Run the command `sudo nano /var/www/html/index.html` and write down the contents of the html script (the same ones as in the index.html of this repository) and save. Confirm whether the index.html has been appended.
6. Reboot the instance. After successful reboot, copy its public IP address and paste it as a URL.


