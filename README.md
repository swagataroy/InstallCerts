* If you want to add the server’s certificate to the KeyStore with your trusted certificates, a simple solution is to compile and 
run this program as java InstallCert hostname, for example
* java InstallCert ecc.fedora.redhat.com
* java InstallCert self-signed.badssl.com:443
* If you've changed your mind, enter 'q'. If you really want to add the certificate, enter '1'
* Once you have made your choice, the program will display the complete certificate and then added it to a Java KeyStore named 'jssecacerts' in the current directory.
* To use it in your program, either configure JSSE to use it as its trust store or copy it into your $JAVA_HOME/jre/lib/security directory. If you want all Java applications to recognize the certificate as trusted and not just JSSE, you could also overwrite the cacerts file in that directory.


