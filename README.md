# NXP-eMPC-Platoon-Control-Algorithm-Evaluation-Platform

This is a guide for using the embedded MPC platoon control algorithm evaluation platform. The platform and installation instructions are based on https://github.com/sijiezhu/NXP-Platoon-Control-Algorithm-Evaluation-Platform/

## Getting Started
### Connections

A Linux PC (or virtual machine) needs to be connected to the MK5 nodes via the Ethernet switch.
**Note**: Make sure the devices in the LAN (local-area network) are all interconnected. This can be checked by SSH commands, for example
```
ssh fe80::6e5:48ff:fe20:0064
```
Sometimes you need to specify the network interface name to connect to the MK5 devices.
```
ssh fe80::6e5:48ff:fe20:0064%eth0
```
### Installation
Unzip the project zip file. The generated folder includes a folder ("llc-platooning-app") containing the source code and a Makefile realizing test automation.

1. Move the "llc-platooning-app" to "mk5/stack/apps"

2. Create a project directory in "workspace-mk5" and shortcut to the source code.
```
cd workspace-mk5
mkdir PCA_test_fgm
cd PCA_test_fgm
ln -s ~/mk5/stack/apps/llc-platooning-app ./
```
3. Move the unzipped Makefile to "workspace-mk5/PCA_test_fgm/".

4. For successfully executing the example, the *MK5 IP addresses* and the log directory *$(LOG_DIR)* in the *Makefile* might need to be modified.

5. For further information on the platform and how to run it, see the "Thesis.pdf" document attached. The running instructions can be found in Appendix A. 

## Authors

* **Iñaki Martín Soroa** -  [Github](https://github.com/inkms)
