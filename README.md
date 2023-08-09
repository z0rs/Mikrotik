# MikroTik SMB Remote Denial of Service (DoS)

The Server Message Block (SMB) protocol was introduced by Microsoft and reimplemented by multiple vendors in order to maintain file exchange compatibility to Windows systems and services. The protocol in general is used for file exchange between Windows systems.

## using

please rebuild the used test environment provided in this repo.

   1. Download and start the RouterOs environment.

        Please execute the following script on a fresh installed version of
        Ubuntu 18.04, since *the script will install all required software*.
        The script ends by providing the IP of the RouterOs VM.

        ```bash
        sudo ./setupMikroTikEnvironment.sh
        ```
   2. Enable SMB on RouterOs

        Run the following commands to activate the SMB service.

        ```bash
        telnet <RouterOs IP>
        (user: admin, <no password>)
        ip smb set enabled=yes
        ip smb print
        ```
        The service can be checked manually from the host system with the following command and should respond
        wiht `Anonymous login successful` as long the service is running.

        ```bash
        smbclient -N -L \\\\<RouterOs IP>
        ```
 3. The denial of service attack

        The python3 script `testing.py` validates the availability of the SMB service before and after the
        exploitation process. A successful execution will end up with the unavailability of the SMB service.
        Please execute the script as shown below.

        ```python
        python3 testing.py --ip <RouterOs Ip>
        ```

        Testing the SMB service with the following command will fail.

        ```bash
        smbclient -N -L \\\\<RouterOs IP>
        ```
        
  4. Remove VM

        In order to remove the VM just run the script again.

        ```bash
        sudo ./setupMikroTikEnvironment.sh
        ```
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
Auto commit
