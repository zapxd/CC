# Viva Questions and Answers – Google App Engine (GAE) Setup

### 1. What is Google App Engine?
**Answer:**  
Google App Engine (GAE) is a Platform as a Service (PaaS) offering from Google that allows developers to build and deploy web applications on Google’s infrastructure. It abstracts server management and allows developers to focus on writing code.

---

### 2. How does Google App Engine work?
**Answer:**  
Google App Engine works by allowing developers to upload web applications, which are then managed and scaled automatically by Google. It uses sandboxed environments and supports multiple languages. GAE applications are deployed using an `app.yaml` configuration file that defines routes and runtime.

---

### 3. What are the different versions of Google App Engine?
**Answer:**  
Google App Engine has two main environments:
- **Standard Environment:** Uses sandboxing and supports a limited set of languages and versions (like Python 2.7, 3.7+).
- **Flexible Environment:** Offers more freedom with custom runtimes and access to the full OS, suitable for more complex applications.

---

### 4. What is the purpose of `app.yaml` in GAE?
**Answer:**  
The `app.yaml` file defines the configuration for a GAE application. It includes:
- Application ID
- Version
- Runtime
- URL handlers (routing)
It acts as the entry point for GAE to understand how to route requests.

---

### 5. Why is Python 2.5.4 used for this GAE setup?
**Answer:**  
Python 2.5.4 is used because the earlier versions of Google App Engine SDK required Python 2.5 to run local development servers and support deployed applications. Newer SDKs support later Python versions.

---

### 6. How do you run a GAE application using the GAE Launcher?
**Answer:**  
- Open GAE Launcher
- Add an existing application folder
- Click **Run**
- Click **Browse** to view the app at `http://localhost:8080/`

---

### 7. What is the URL to view your local GAE app?
**Answer:**  
`http://localhost:8080/`

---

### 8. What does the `index.py` file do in a GAE app?
**Answer:**  
The `index.py` file is the script that handles HTTP requests routed from GAE. It typically outputs HTTP headers and a response message like "Hello World".

---

### 9. How do you debug an error in `app.yaml`?
**Answer:**  
Check the GAE Launcher logs. If the application fails to start, it's usually due to indentation or syntax errors in `app.yaml`.

---

### 10. How do you fix a syntax error in `index.py`?
**Answer:**  
Edit the file in a text editor, correct the syntax, and simply refresh the browser. You don’t need to restart the server.

---

### 11. How do you stop the GAE server?
**Answer:**  
Use the GAE Launcher, select your app, and click the **Stop** button.

---

### 12. What is Eclipse IDE?
**Answer:**  
Eclipse is an integrated development environment (IDE) used in computer programming. It supports multiple languages like Java, C++, Python, etc., and offers tools for development, debugging, and deployment.

---

### 13. What are the advantages of using GAE?
**Answer:**  
- No server management
- Automatic scaling
- Built-in security and load balancing
- Integrated with Google Cloud services

---

### 14. What is the default port for local GAE apps?
**Answer:**  
Port **8080**

---

### 15. What is the purpose of the GAE development server?
**Answer:**  
It simulates the App Engine runtime environment on your local machine, allowing you to test and debug applications before deployment.

# Viva Questions and Answers – File Transfer Between Virtual Machines

### 1. What is virtualization?
**Answer:**  
Virtualization is the process of creating a virtual version of computing resources such as operating systems, servers, storage devices, or network resources. It allows multiple operating systems to run on a single physical machine.

---

### 2. What is the difference between host and guest machines?
**Answer:**  
The host machine is the actual physical computer on which the virtualization software (hypervisor) is installed. The guest machine is the virtual machine running on the host, simulating a separate physical computer with its own OS.

---

### 3. What is a hypervisor?
**Answer:**  
A hypervisor, or Virtual Machine Monitor (VMM), is software, firmware, or hardware that creates and manages virtual machines. It allocates hardware resources to each VM and ensures isolation.

---

### 4. What are the types of virtualization mentioned?
**Answer:**  
- **Operating-system-level virtualization:** Multiple isolated user-space instances are created using the same kernel.
- **Platform/Hardware virtualization:** Virtual machines simulate physical hardware, allowing different OSs to run on a single host.

---

### 5. What is Oracle VirtualBox?
**Answer:**  
Oracle VirtualBox is an open-source, general-purpose virtualizer for x86 hardware, which allows users to run multiple operating systems on a single physical machine.

---

### 6. What is Ubuntu?
**Answer:**  
Ubuntu is a free and open-source Linux-based operating system. It can be freely downloaded, modified, and installed on any number of systems.

---

### 7. How do you configure a NAT Network in VirtualBox?
**Answer:**  
- Go to File → Preferences → Network
- Click the "+" button to add a new NAT Network
- Edit the network name and CIDR (e.g., 172.168.2.0/24)
- Save the configuration

---

### 8. What is a VMDK file?
**Answer:**  
A VMDK (Virtual Machine Disk) file is a virtual disk file used by virtual machines. It stores all the data on a virtual machine’s hard disk.

---

### 9. How can you find the IP address of a VM?
**Answer:**  
First, install `net-tools` using:
```bash
$ sudo apt install net-tools
$ sudo apt update
```
Then run:
```bash
$ ifconfig
```
This command will display the IP address assigned to the VM.

---

### 10. What is SCP and how is it used?
**Answer:**  
SCP (Secure Copy Protocol) is a command-line tool used to securely transfer files between hosts on a network using SSH.  
Example:
```bash
$ scp file.txt username@destination_IP:/path/to/destination
```

---

### 11. What is the command to transfer a file from one VM to another?
**Answer:**  
Assuming the sender VM's IP is `172.168.2.4` and the receiver VM's IP is `172.168.2.5`, the command is:
```bash
$ scp transfer.txt vagrant@172.168.2.5:/home/vagrant
```

---

### 12. What are some basic Linux commands used during this procedure?
**Answer:**  
- `ls` – List files and directories  
- `cat` – View file contents  
- `cd` – Change directory  
- `mkdir` – Create a new directory  
- `touch` – Create a new file  
- `nano` – Text editor to edit files  
- `ifconfig` – Show network configuration  
- `scp` – Secure copy to transfer files

---

### 13. Why do we use a NAT Network for communication between VMs?
**Answer:**  
A NAT Network allows multiple VMs to communicate with each other through virtual IP addresses without needing physical network access, ensuring isolation and ease of setup.

---

### 14. What is the use of `nano` command?
**Answer:**  
`nano` is a simple command-line text editor used to create and edit text files in Linux.

---

### 15. What is the default range of IPs in the CIDR `172.168.2.0/24`?
**Answer:**  
The IP range spans from `172.168.2.1` to `172.168.2.254`, supporting up to 254 devices on the same subnet.

### Viva Questions and Answers: TryStack (OpenStack Demo)

#### Q1. What is OpenStack?
**A:** OpenStack is an open-source cloud computing platform primarily used to deploy infrastructure as a service (IaaS). It allows users to create and manage large networks of virtual machines.

#### Q2. What is TryStack?
**A:** TryStack is a free, online demo platform of OpenStack. It allows users to test and understand OpenStack features without installing it locally.

#### Q3. What are the minimum system requirements for running OpenStack?
**A:**
- 4 GB of RAM
- 4 CPU units
- 30 GB disk space

#### Q4. Why do we create a "stack" user for installing OpenStack?
**A:** OpenStack is usually installed under a non-root user for security and configuration isolation. The "stack" user is used with sudo privileges to perform the installation and management tasks.

#### Q5. Which command is used to download the DevStack repo?
**A:** 
```bash
git clone https://git.openstack.org/openstack-dev/devstack
```

#### Q6. What is the purpose of `local.conf` file in OpenStack installation?
**A:** The `local.conf` file is used to automate the OpenStack installation by pre-defining passwords for services like the admin panel, database, RabbitMQ, and identity service.

#### Q7. How do you start the OpenStack installation using DevStack?
**A:** Use the command `./stack.sh` inside the `devstack` directory.

#### Q8. How do you access the OpenStack dashboard?
**A:** Once installation is complete, the dashboard can be accessed using the URL: `http://<IPAddress>/dashboard/`

#### Q9. What is the significance of creating a network before launching an instance?
**A:** Without a network, instances cannot be launched or connected to the internet. The network allows VMs to communicate internally and externally.

#### Q10. What is a "Flavor" in OpenStack?
**A:** A flavor defines the compute, memory, and storage capacity of virtual machines. It is similar to setting up hardware specs for your VM.

#### Q11. What are the steps to launch an instance in OpenStack?
**A:**
1. Go to "Project" → "Compute" → "Instances"
2. Click on "Launch Instance"
3. Fill in the 11 tabs (Details, Source, Flavor, Network, etc.)
4. Click "Launch Instance"

#### Q12. What is "Cirros" in the context of OpenStack?
**A:** Cirros is a minimal Linux distribution used for testing purposes in cloud environments. It is commonly used as the base image to launch VMs in OpenStack.

#### Q13. What is the function of the "Security Groups" tab while launching an instance?
**A:** Security groups define firewall rules for instances, controlling how VMs communicate with each other and external networks.

#### Q14. How do you access the virtual machine once it is launched?
**A:** You can access the VM using the "Console" option from the OpenStack dashboard.

#### Q15. What is the role of the "Key Pair" tab?
**A:** The Key Pair tab allows users to configure SSH access to the instance. However, it can be skipped if not required during demo usage.

#### Q16. What is the purpose of the DevStack tool?
**A:** DevStack is a collection of scripts used to quickly deploy OpenStack for development and testing purposes.

#### Q17. Why do we run `sudo apt-get update` and `sudo apt-get upgrade` before installation?
**A:** These commands ensure that all packages are up-to-date and prevent issues during the OpenStack installation process.

#### Q18. What is the function of the `sudo reboot` command after setup?
**A:** It reboots the system to apply updates and ensure a clean state before starting the OpenStack installation.

#### Q19. Can we run OpenStack on Windows?
**A:** OpenStack is designed to run on Linux-based systems. However, it can be tested via virtual machines on Windows using platforms like VirtualBox.

#### Q20.