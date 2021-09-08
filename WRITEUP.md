# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

As a very simple, lightweight project, the cost for thje CMS app should be kept as low as possbile. Also  scalability is not something to worry about as no increase in traffic is expected any time soon.  Both Azure App Service and VM very high availabilty, with over 99.95% for App Service and at least 95% for a VM (that is for Standard HDD Managed Disks for Operating System Disks and Data Disks, higher SLA for SDD Managed Disks). The app can be deployed easily from github using while using an App Service, while there are several intermediate steps (with nginx) while working with a Virtual Machine. 

I chose to deploy the app using App Service, as it was much simpler and faster to do so; without sacrificing availability and cost. This way, I won't have to worry about maintaining a virtual machine. For this app, if for scaling reasons I had to change my decision, I will probably still go for an App Service that is not free with a higher size and Sku, and revert to using a virtual machine as a last resort