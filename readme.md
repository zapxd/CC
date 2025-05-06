
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
```
$ sudo apt install net-tools
$ sudo apt update
```
Then run:
```
$ ifconfig
```
This command will display the IP address assigned to the VM.

---

### 10. What is SCP and how is it used?
**Answer:**  
SCP (Secure Copy Protocol) is a command-line tool used to securely transfer files between hosts on a network using SSH.  
Example:
```
$ scp file.txt username@destination_IP:/path/to/destination
```

---

### 11. What is the command to transfer a file from one VM to another?
**Answer:**  
Assuming the sender VM's IP is `172.168.2.4` and the receiver VM's IP is `172.168.2.5`, the command is:
```
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

#### Q20. What are the different sources available in the "Source" tab for launching an instance?
**A:**
- Image
- Snapshot
- Volume
- Volume Snapshot



### Viva Questions and Answers: Salesforce Lightning Custom Application

#### Q1. What is Salesforce?
**A:** Salesforce is a cloud-based software company that provides customer relationship management (CRM) services. It helps businesses manage customer data, sales processes, marketing automation, and service support through a unified platform.

#### Q2. What is the Salesforce Lightning Experience?
**A:** Salesforce Lightning Experience is a modern user interface for Salesforce applications. It includes a component-based framework for app development and enhanced user experiences like the Lightning App Builder, Lightning Components, and Lightning Sync.

#### Q3. What is the purpose of creating a Custom Object in Salesforce?
**A:** A Custom Object allows users to create a tailored data structure specific to their business needs. In this project, a Custom Object is used to manage student details such as email, phone, and date of birth.

#### Q4. How do you create a Custom Object in Salesforce Lightning?
**A:**
1. Log into the Salesforce Developer account.
2. Navigate to Object Manager → Create → Custom Object.
3. Fill in required details and enable "Allow Reports" and "Allow Activities".
4. Click Save.

#### Q5. What types of fields were added to the Custom Object in the project?
**A:** Email, Phone, and Date of Birth fields were added to the Custom Object named Student_Detail.

#### Q6. What is the purpose of creating a Tab in Salesforce?
**A:** Tabs provide navigation to access custom objects directly from the Salesforce interface. It makes the custom object accessible via the UI.

#### Q7. How do you create a new Tab for a Custom Object?
**A:**
1. Search for "Tabs" in the Setup menu.
2. Click "New" and select the Custom Object.
3. Choose a Tab style and icon.
4. Save the configuration.

#### Q8. What is a Lightning App in Salesforce?
**A:** A Lightning App is a custom app built using the Lightning App Builder that bundles together related objects, tabs, and functionalities to create a dedicated workspace for users.

#### Q9. What was the name of the Lightning App created in the mini project?
**A:** The Lightning App created was named **Student Details Manager**.

#### Q10. What are the steps to create a Lightning App in Salesforce?
**A:**
1. Go to App Manager and click "New Lightning App".
2. Set the App Name and Developer Name.
3. Configure app options and utility settings (leave defaults).
4. Add navigation items like Student_Detail.
5. Assign user profiles (e.g., System Administrator).
6. Save and Finish.

#### Q11. How do you launch and test the custom application?
**A:**
1. Use the App Launcher to open the custom app.
2. Click on the custom object tab (Student_Detail) → New → Enter data.
3. Copy the record URL.
4. Open Developer Tools in Google Chrome and paste the URL to inspect the interface.

#### Q12. What is the use of Developer Tools in this context?
**A:** Developer Tools are used to inspect HTML, CSS, and JavaScript code and debug user interface issues. It helps verify how the application behaves on the client side.

#### Q13. What are some key advantages of using Salesforce Lightning over Classic?
**A:**
- Enhanced user interface and user experience
- Drag-and-drop app builder (Lightning App Builder)
- Component-based development
- Better integration with modern cloud features

#### Q14. What is the use of the “Allow Reports” option while creating a custom object?
**A:** It enables reporting features on the custom object, allowing users to create reports using the data from that object.

#### Q15. Why do we assign the application to a specific user profile?
**A:** Assigning user profiles like System Administrator ensures that only authorized users can access or manage the application components.

#### Q16. Can Lightning Apps be used on mobile devices?
**A:** Yes, Salesforce Lightning Apps are mobile-responsive and accessible via the Salesforce mobile app.

#### Q17. What is Lightning App Builder?
**A:** It is a point-and-click tool in Salesforce that allows users to build custom pages for Lightning Experience and Salesforce mobile app using components.

#### Q18. What is a Developer Edition in Salesforce?
**A:** It is a free, fully-featured Salesforce environment used for learning, testing, and developing applications without affecting production data.

#### Q19. Can you deploy this custom app to production?
**A:** Yes, after proper testing, the custom app can be deployed to a production org using change sets or Salesforce deployment tools like ANT or Salesforce DX.

#### Q20. What are some limitations of the Salesforce Developer Edition?
**A:**
- Limited storage
- Limited API calls
- Restricted number of users and features

### Viva Questions and Answers: Cloud Computing Lab Assignments (314458)

#### Q1. What is Google App Engine (GAE)?
**A:** Google App Engine is a Platform as a Service (PaaS) provided by Google Cloud that enables developers to build and deploy applications without managing the underlying infrastructure.

#### Q2. What is the use of the GAE Launcher?
**A:** GAE Launcher is a graphical tool used to develop, test, and deploy Python-based web applications to Google App Engine. It helps simulate the production environment locally.

#### Q3. What are the steps to launch a web application using GAE Launcher?
**A:**
1. Create an application directory with `app.yaml` and main code file.
2. Open GAE Launcher and add the application.
3. Run the app locally to test.
4. Deploy it to Google App Engine using the launcher or `gcloud app deploy`.

#### Q4. What is required in the `app.yaml` file for a GAE application?
**A:** The `app.yaml` file contains the configuration for the application such as runtime, instance class, handlers, and automatic scaling settings.

#### Q5. What are the methods to transfer files between two virtual machines?
**A:** Files can be transferred between virtual machines using:
- **SCP (Secure Copy Protocol)**: `scp file.txt user@remote:/path`
- **rsync**: Efficient file sync tool: `rsync -avz file.txt user@remote:/path`
- **Shared Cloud Storage**: Use services like Google Cloud Storage or AWS S3 to share files.

#### Q6. What is SCP and how is it used?
**A:** SCP (Secure Copy Protocol) is a method for securely transferring files between hosts over SSH. It encrypts both file and authentication data.

#### Q7. What is PaaS? Give an example.
**A:** Platform as a Service (PaaS) is a cloud computing model that provides a platform allowing customers to develop, run, and manage applications. Example: Google App Engine, Heroku.

#### Q8. What are the steps to deploy a web app in a PaaS environment?
**A:**
1. Write the application code.
2. Add configuration files (e.g., `app.yaml` for GAE).
3. Use CLI tools like `gcloud` to deploy the app.
4. Monitor and scale through the cloud console.

#### Q9. What is Firebase Authentication?
**A:** Firebase Authentication is a service that allows you to authenticate users using only client-side code, with support for email/password, Google, Facebook, and other providers.

#### Q10. How do you retrieve and store user credentials using Firebase Authentication?
**A:** By integrating Firebase SDK in your application, users can register/login. Their credentials can be verified through Firebase and stored securely using Firestore or Google Cloud Datastore.

#### Q11. What is Google Cloud Datastore?
**A:** Google Cloud Datastore is a highly scalable NoSQL database service for web and mobile apps, used to store non-relational structured data.

#### Q12. How do GAE, Firebase Auth, and Cloud Datastore work together?
**A:**
- Firebase handles user sign-up/sign-in and token generation.
- GAE hosts the backend logic (e.g., processing requests).
- Cloud Datastore stores persistent user data like profiles, roles, etc.

#### Q13. What is the standard environment in Google App Engine?
**A:** The standard environment is a sandboxed runtime (Python, Java, Node.js, etc.) with automatic scaling and fast deployments, ideal for stateless applications.

#### Q14. How does Firebase ensure security while storing user data?
**A:** Firebase uses secure authentication tokens, rules-based access control, and encryption (at rest and in transit) to protect user data.

#### Q15. Can Firebase Authentication be used without Google App Engine?
**A:** Yes, Firebase Authentication can be used with any frontend or backend platform, not just GAE. However, integrating with GAE allows more scalable backend services.

#### Q16. What is the role of `firebase.initializeApp()` in a web app?
**A:** It initializes your Firebase project with configuration settings (API key, project ID, etc.) allowing you to use services like Authentication and Firestore in your app.

#### Q17. Why is GAE considered suitable for deploying scalable web apps?
**A:** GAE offers features like automatic scaling, versioning, traffic splitting, and built-in security which make it suitable for scalable and reliable web applications.

#### Q18. How can you view logs of your application deployed on GAE?
**A:** Logs can be viewed using:
- Google Cloud Console (Logs Explorer)
- `gcloud app logs read` command in terminal

#### Q19. What is the difference between Google Cloud Storage and Google Cloud Datastore?
**A:** Cloud Storage is for storing unstructured binary data like images, videos, and backups. Cloud Datastore is for structured NoSQL data like user records and objects.

#### Q20. What is IAM in Google Cloud?
**A:** IAM (Identity and Access Management) controls who (users) has what access (roles) to which resources in a Google Cloud project.





