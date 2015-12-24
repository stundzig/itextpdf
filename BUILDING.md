To build iText, [Maven][1] must be installed.

Running install without a profile will generate the itextpdf jar:
```bash
$ mvn install
```

When using the profile 'all' also the source and javadoc jars will be generated:
```bash
$ mvn install -P all
```

If you are in need of the Asian font jars, you can run one of the following commands:
```bash
$ mvn clean install -f itextpdf/itext-asian.pom
```

If you need the hyphenation jar, execute:
```bash
$ mvn clean install -f itextpdf/itext-hyph-xml.pom
```

To run the tests, [Ghostscript][2] and [Imagemagick][3] must be installed.

You can use the `Vagrantfile` to get a [Vagrant][4] VM ([Ubuntu][5] 14.04 LTS - Trusty Tahr, with [VirtualBox][6]) with all the required software installed.
```bash
$ vagrant box add ubuntu/trusty64
$ vagrant up
$ vagrant ssh
$ cd /vagrant
$ mvn install
```

[1]: http://maven.apache.org/
[2]: http://www.ghostscript.com/
[3]: http://www.imagemagick.org/
[4]: https://www.vagrantup.com/
[5]: http://www.ubuntu.com/
[6]: https://www.virtualbox.org/