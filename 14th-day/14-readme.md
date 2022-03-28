# 28-March-2022- 14th class reading notes:

## AWS: Cloud Servers:

### **Introduction**

Amazon Web Services, Inc. is a subsidiary of Amazon providing on-demand cloud computing platforms and APIs to individuals, companies, and governments, on a metered pay-as-you-go basis. These cloud computing web services provide a variety of basic abstract technical infrastructure and distributed computing building blocks and tools. One of these services is Amazon Elastic Compute Cloud, which allows users to have at their disposal a virtual cluster of computers, available all the time, through the Internet. AWS's virtual computers emulate most of the attributes of a real computer, including hardware central processing units and graphics processing units for processing; local/RAM memory; hard-disk/SSD storage; a choice of operating systems; networking; and pre-loaded application software such as web servers, databases, and customer relationship management.

**What is AWS**
Cloud computing with AWS
Amazon Web Services (AWS) is the world’s most comprehensive and broadly adopted cloud platform, offering over 200 fully featured services from data centers globally. Millions of customers—including the fastest-growing startups, largest enterprises, and leading government agencies—are using AWS to lower costs, become more agile, and innovate faster.

### **AWS EC2**

AWS EC2 is one of the most important services AWS offers. Getting started with it can be simple and hard at the same time. With this video, we'll focus on the simple part. And make the hard part simple, too.

* Install a LAMP web server on the Amazon Linux AMI
  1. Prepare the LAMP server
  2. Test your Lamp server
  3. Secure the database server
  4. (Optional) Install phpMyAdmin

[more details:] (https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-LAMP.html)

* Connect to your Linux instance
  * Connection options
    The operating system of your local computer determines the options that you have to connect from your local computer to your Linux instance.

    If your local computer operating system is Linux or macOS X
    - SSH client
    - EC2 Instance Connect
    - AWS Systems Manager Session Manager

    If your local computer operating system is Windows
    - PuTTY
    - SSH client
    - AWS Systems Manager Session Manager
    - Windows Subsystem for Linux

**AWS Elastic Beanstalk**
is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

You can simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time.

There is no additional charge for Elastic Beanstalk - you pay only for the AWS resources needed to store and run your applications.

**Benefits**
 - Impossible to outgrow
 - Fast and simple to begin
 - Developer productivity
 - Complete resource control


## **Virtual Machine**

In computing, a virtual machine (VM) is the virtualization/emulation of a computer system. Virtual machines are based on computer architectures and provide functionality of a physical computer. Their implementations may involve specialized hardware, software, or a combination.

**Types of virtualization**
Therefore, software and hardware manufacturers have begun to address some of these concerns by shifting how traditional data centers are architected via virtualization. There are the various types of virtualization:

- Hardware virtualization:
Virtualizing hardware, including versions of computers and operating systems (VMs), creates a single, virtual, consolidated, primary server.

- Software virtualization:
Creates a computer system, including hardware, that allows one or more guest OS to run on a physical host machine.

- Storage virtualization:
Virtualizes storage by consolidating multiple physical storage devices, which appear as a single storage unit for improved performance and increased speed.

- Network virtualization:
Enables application-driven cloud virtual networking across an entirely distributed set of systems, decoupling from physical network infrastructure. Network virtualization allocates bandwidth across channels, providing resources to servers and devices in real-time.

- Desktop virtualization:
Separates your desktop environment from the physical device and stores a desktop on a remote server, allowing access from anywhere on any device.

**Containers vs. virtual machines**
Containers and virtual machines are both used by developers and IT professionals to create isolated virtual environments for testing and developing software. Whereas a virtual machine depends on a host to run a complete operating system, a container is an isolated silo that runs an application on the host. Containers run applications that are not dependent on an operating system—rather, they isolate an application by virtualizing it.

Since containers don’t contain operating systems, containers are lightweight and more portable than virtual machines. And even though containers are portable, they’re still constrained by their operating system; so that a container for Windows is unable to run on Linux. In the end, deciding between a container or a virtual machine depends on how a virtual environment will be used.

**What are VMs used for?**
Here are a few ways virtual machines are used:

1. Building and deploying apps to the cloud.
2. Trying out a new operating system (OS), including beta releases.
3. Spinning up a new environment to make it simpler and quicker for developers to run dev-test scenarios.
4. Backing up your existing OS.
5. Accessing virus-infected data or running an old application by installing an older OS.
6. Running software or apps on operating systems that they weren't originally intended for.

**What are the benefits of using VMs?**

Because of their flexibility and portability, virtual machines provide many benefits, such as:

1. **Cost savings—**
    running multiple virtual environments from one piece of infrastructure means that you can drastically reduce your physical infrastructure footprint. This boosts your bottom line—decreasing the need to maintain nearly as many servers and saving on maintenance costs and electricity.
2. **Agility and speed—**
   Spinning up a VM is relatively easy and quick and is much simpler than provisioning an entire new environment for your developers. Virtualization makes the process of running dev-test scenarios a lot quicker.
3. **Lowered downtime—**
   VMs are so portable and easy to move from one hypervisor to another on a different machine—this means that they are a great solution for backup, in the event the host goes down unexpectedly.
4. **Scalability—**
   VMs allow you to more easily scale your apps by adding more physical or virtual servers to distribute the workload across multiple VMs. As a result you can increase the availability and performance of your apps.
5. **Security benefits—** 
   Because virtual machines run in multiple operating systems, using a guest operating system on a VM allows you to run apps of questionable security and protects your host operating system. VMs also allow for better security forensics, and are often used to safely study computer viruses, isolating the viruses to avoid risking their host computer.

[Introduction to Virtualization](https://www.youtube.com/watch?v=l0DfHUWMjsU)
[EC2 for Humans](https://www.youtube.com/watch?v=lZMkgOMYYIg)