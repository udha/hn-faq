# Hosts File <small>FAQ</small>

## About hosts files

A `#!cirru hosts` file can be used to override the DNS for your domain name. This is ideal for testing new site hosting before making any public DNS changes, so that you can confirm everything is working right.

To point `#!cirru myexample.com.au` domain to `#!cirru 202.174.108.4` using your `#!cirru hosts` file we will simply need to add the following lines into the `#!cirru hosts` file: 

``` cirru
202.174.108.4   myexample.com.au
202.174.108.4   www.myexample.com.au
```

??? info "Advanced `#!cirru IPv6` tips:"

    Manually Set an `#!cirru IPv6 AAAA record`:
    ``` cirru
    2402:e400::0     myexample.com.au
    2402:e400::0     www.myexample.com.au
    ```

    Override existing `#!cirru IPv6 AAAA records` with an `#!cirru IPv4` address:

    ``` cirru
    ::202.174.108.4   myexample.com.au
    ::202.174.108.4   www.myexample.com.au
    ```

---

## How-To

For modern Windows users open the start menu and type `#!cirru notepad` to have the built-in search locate the **Notepad** <small>*Desktop App*</small>. Then `right-click` on it and select `Run as administrator`:

![Run Notepa as Administrator](/img/hostsfile/StartMenu_Notepad_RunAsAdmin.png)

---

Within `Notepad` click `File > Open...` and type or copy-paste the following `File name`:

``` cirru
C:\Windows\system32\drivers\etc\hosts
```

![Notepad > Open > c:\windows\system32\drivers\etc\hosts](/img/hostsfile/Notepad_Open_win-sys32-drivers-etc-hosts.png)

---

Once you have clicked `Open` you will see the contents of your `#!cirru hosts` file. This is where we add the IP address followed by the domain name on a new line, in our example we will add the following:

``` cirru
202.174.108.4   myexample.com.au
202.174.108.4   www.myexample.com.au
```

![Notepad > Open > c:\windows\system32\drivers\etc\hosts](/img/hostsfile/Notepad_hosts_myexample.com.au.png)

---

Remember to `Save` the changes in `notepad` before we `#!cirru ping` to test the changes made:

``` cirru
ping www.myexample.com.au
```

![cmd.exe > ping www.myexample.com.au](/img/hostsfile/cmd_ping_myexample.com.au.png)

---

## Cleaning Up

As long as these lines remain in the `#!cirru hosts` file the DNS override will be in effect for your PC, so always be sure to remove any additions made to your `#!cirru hosts` file when you have finished your testing.

---

# Further Resources

> Still in need of help? For speedy assistance our friendly staff are always ready to help via our [helpdesk](https://helpdesk.hostnetworks.com.au/core/), on [Twitter](https://twitter.com/HostNetworks), through our [website](https://hostnetworks.com.au/), or directly via [email to support](/contact/).

---

