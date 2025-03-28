# Audi UTR Dashcam

## Finding 1 - CVE-2025-30118: Audi UTR Susceptibility to DoS
**Description**: An issue was discovered on the Audi Universal Traffic Recorder 2.88. It has susceptibility to denial-of-service. It uses the same default credentials for all devices and does not implement proper multi-device authentication, allowing attackers to deny the owner access by occupying the only available connection. The SSID remains broadcast at all times, increasing exposure to potential attacks.

**Vulnerability Type**: Incorrect Access Control

**Vendor of Product**: Audi

**Affected Product Code Base**: Audi Universal Traffic Recorder 2.88

**Affected Component**: Device network access control

**Attack Type**: Remote

**Impact Denial of Service**: true

**Attack Vectors**: The dashcam allows only one connected device at a time. An attacker can connect via Wi-Fi cracking and prevent the owner from accessing the device. The SSID is always broadcasted, making it easily detectable.


## Finding 2 - CVE-2025-2555: Hardcoded Credentials in AUDI Universal Traffic Recorder < App v2.89
AUDI UTR Dashcam’s companion app contains hardcoded FTP credentials, allowing unauthorized attackers to gain access to the dashcam’s network and functions.
The application contains a hardcoded password ("wificam") that can be easily retrieved by searching the APK for "password".

## Finding 3 - CVE-2025-2556: RTSP and FTP wide open
AUDI UTR Dashcam allows unauthorized access to RTSP video streaming and FTP file storage using hardcoded credentials. Attackers can extract all recorded footage and monitor live streams remotely.

![image](https://github.com/user-attachments/assets/13a682a1-dcbe-4fd2-9f60-066d7ab7f888)

![image](https://github.com/user-attachments/assets/add1fc09-ca7c-4d01-a9be-8a713d9e1032)


## Finding 4 - CVE-2025-2557: Execute Remote Commands
Using the Audi UTR APK, an attacker can obtain a list of remotely executable commands once logged on using weak/default credentials. For instance, getting userdata, calling for factory reset, or even trigger a malicious firmware update to "/sd/DSM_FW.muf".

![image](https://github.com/user-attachments/assets/2623a67a-a649-435a-a927-044e060811b4)

## Disclosure

20 Feb 2025 - Reported to Audi

20 Feb 2025 - Audi confirmed receipt

7 Mar 2025 - Sent fow up to Audi

10 Mar 2025 - Audi accepted and started investigating

17 Mar 2025 - Receive thanks. Audi deploys app update v2.89 to improve wifi encryption. v2.90 is also scheduled with additional hardening.



