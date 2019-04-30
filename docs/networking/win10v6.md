# Windows 10 <small>IPv6</small>

## Allow ICMPv6 Ping Reply

Windows unfortunately blocks certain ICMPv6 packets by default. This becomes a nuisance when troubleshooting and testing IPv6 networking from a Windows system.

## Step-by-step Instructions

### Permit ICMPv6 in Windows 10

---

Open **Start / Run** then type: `#!cirru wf.msc` 

Press **Enter** or click **OK** to open a Microsoft Management Console with the **Windows Defender Firewall with Advanced Security** snap-in

---

From the Firewall settings select **Inbound Rules** and click **New Rule…** On the **Rule Type** page, select **Custom** and click **`Next >`**

---

Select **All programs** and click **`Next >`**

---

Change **Protocol type** to **ICMPv6** then click **`Next >`**

![Protocol and Ports - ICMPv6](/img/win10v6/Win10v6ProtoTypeICMPv6.png)

---

Leave the **Scope** unchanged  and click **`Next >`** *(Default scope is Any IP address)*

---

Ensure **Allow the connection** is selected then click **`Next >`**

---

Select your required profiles and click **`Next >`**

---

Enter a name, we went with **Permit All ICMPv6** and click **Finish**

---

# Further Resources

> Still in need of help? For speedy assistance our friendly staff are always ready to help via our [helpdesk](https://helpdesk.hostnetworks.com.au/core/), on [Twitter](https://twitter.com/HostNetworks), through our [website](https://hostnetworks.com.au/), or directly via [email to support](/contact/).

---

