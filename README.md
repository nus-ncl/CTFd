[Original README](https://github.com/CTFd/CTFd/blob/master/README.md)

[Deployment Guide](https://github.com/nus-ncl/ctfd-deployment/blob/master/Deployment_Guides/core/ctfd-core-deployment.txt)

**WORK-IN-PROGRESS**

CTFd now takes in an additional arguments 

--ncl-sio-url for NCL SIO URL
--ncl-team-name for name of the NCL Team whose members are allowed to login

```
uwsgi --plugin python -s /tmp/uwsgi1.sock -w 'CTFd:create_app()' --chmod-socket=666 --pidfile /tmp/ctfd1.pid --pyargv '--ncl-sio-url http://172.18.178.14:8080 --ncl-team-name ncltest01'
```

## Changes made by [Ong Heng Le](https://github.com/initialshl)

6 July 2018 : https://github.com/nus-ncl/CTFd/commit/b8922ed92f80dcf2245ca546366999b886331aae

- Login now checks that the user is part of the specified NCL Team

3 July 2018 : https://github.com/nus-ncl/CTFd/commit/af37fec42bbe34aa2825688aaf40dc1cb4fc6a89

- "Register"/"Forgot Password" opens a new tab in NCL
- Users can change only their name in their profile page
- Initial CTFd setup can now be done using deployment scripts

2 July 2018 : https://github.com/nus-ncl/CTFd/commit/d3979e74bc96f412388de892d29d79977a1e6f04

- Login using NCL SIO authentication API
- Disabled user registration
- Disabled user password reset
