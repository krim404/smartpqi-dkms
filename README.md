### Overview

This repository contains a modified version of the Microsemi SmartPQI driver in version 2.1.32.035, tailored to support Linux kernels version 6.11 and newer. The modifications replace deprecated header includes to ensure compatibility with the latest kernel versions.


### Installation

#### Prerequisites

Ensure the following packages are installed on your system:

- `dkms`
- `build-essential`
You can install these on Debian/Ubuntu-based systems using:

```bash
sudo apt-get install dkms build-essential
```


#### Steps

1. Clone the repository:

```bash
git clone https://github.com/krim404/smartpqi-dkms.git
cd smartpqi-dkms
```

2. Copy the driver source to the DKMS directory:

```bash
sudo cp -r . /var/lib/dkms/smartpqi/2.1.32.035/source 
```

3. Add the module to DKMS:

```bash
sudo dkms add -m smartpqi -v 2.1.32.035
```

4. Build and install the module:

```bash
sudo dkms build -m smartpqi
sudo dkms install -m smartpqi
```

5. Load the module:

```bash
sudo modprobe smartpqi
```

