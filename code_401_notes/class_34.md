# Code 401 Reading Notes 
### 34. API Deployment

####  source: "Configuring Django Settings: Best Practices" [link](https://djangostars.com/blog/configuring-django-settings-best-practices/)
- problems with django settings.py files include: different environments, sensitive data, sharing settings between team members, and the fact that Django settings are written in python 
- there are various ways to configure settings: 
  - with a settings_local.py 
  - separate settings.py for each env; implemented with a settings folder that contains things like: 
    - base.py
    - local.py 
    - staging.py 
    - production.py  
  - with env variables 
  - 12 factors approach (stores config in the environment)
- you can store environment vars with django-environ 
- Django settings best practices: 
  - put settings in env variables 
  - write default values for production configuration (except for secret keys and tokens)
  - split settings into groups: Django, third-party, project
- using the env vars approach makes deployment via containers easier 


####  source: Domantas G., "What Is SSH: Understanding Encryption, Ports and Connection" [link](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)
- secure shell protocol allows users to interact with their servers over the internet 
- SSH allows for encrypted transfer of data from host to client 
- three types of encryption include symmetrical encryption, asymmetric encryption, and hashing 
- two stages to setting up a client-server connection: 
  - client and server agree on standards for encryption 
  - client authenticates themselves 
  

#### Things I want to know more about 
- the 12 parts of heroku's suggested deployment 
