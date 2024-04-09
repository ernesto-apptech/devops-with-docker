**T Deployment process:**

I've chosen GCP Compute Engine because I'm more familiar with it from previous projects.

**Virtual Machine Configuration:**

* Machine type: e2-micro/us-central1-c (the most affordable option)
* Firewall default rules: Allow incoming HTTP and HTTPS traffic
* Operating System: Container-Optimized OS (pre-installed Docker)

**Pulling and Running the Docker Image:**

Since the VM with container-Optimized OS already has Docker, we can simply pull the image:

```
docker pull ernestoapptech/project-p1
```

Then, run the container, mapping port 3000 on the host machine to port 8080 inside the container:

```
docker run -p 3000:8080 ernestoapptech/project-p1
```

**Firewall Rule for Port 3000:**

As the application runs on port 3000, we need a firewall rule to allow incoming traffic on TCP port 3000.

**Accessing the Application:**

With the firewall rule in place, you can access the application at `http://34.135.160.5:3000`.

**Important Note:**

* The provided IP address (`34.135.160.5`) is likely an ephemeral IP and will change upon VM restart.
* Without a dedicated domain name, the application URL will be dynamic.
