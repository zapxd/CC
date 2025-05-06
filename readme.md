
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

