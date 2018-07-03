[Original README](https://github.com/CTFd/CTFd/blob/master/README.md)

[Deployment Guide](https://github.com/nus-ncl/ctfd-deployment/blob/master/Deployment_Guides/core/ctfd-core-deployment.txt)

**WORK-IN-PROGRESS**

CTFd now takes in an additional argument --ncl-sio-url for NCL SIO URL

```
uwsgi --plugin python -s /tmp/uwsgi1.sock -w 'CTFd:create_app()' --chmod-socket=666 --pidfile /tmp/ctfd1.pid --pyargv '--ncl-sio-url http://dev.ncl.sg:8888'
```

## Changes made by [Ong Heng Le](https://github.com/initialshl)

3 July 2018 : af37fec42bbe34aa2825688aaf40dc1cb4fc6a89

- "Register"/"Forgot Password" opens a new tab in NCL
- Users can change only their name in their profile page
- Initial CTFd setup can now be done using deployment scripts

2 July 2018 : d3979e74bc96f412388de892d29d79977a1e6f04

- Login using NCL SIO authentication API
- Disabled user registration
- Disabled user password reset