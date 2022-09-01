# Jmeter-taurus-local
Run Jmeter in local machine using taurus framework
=======================================================
JMeter is a very popular open source tool for testing your website or webapp. Although it’s quite powerful, it’s not very easy to use and its reporting abilities are very limited. 
Taurus is a free and open source framework for Continuous Testing which helps you by hiding the complexities of running performance tests. 
Think of it as an automation-friendly wrapper - it cloaks nicely around JMeter, neatly covering all of its complexities and imperfections.
When running JMeter through Taurus you can:
•	Run an existing JMeter script
•	Create a new JMeter script very easily using a YAML text file
•	Automate your script with Jenkins/AzureDevops.

Dependency: 
==============
1.	Get Python 3.7+ from http://www.python.org/downloads and install it, don't forget to enable "Add python.exe to Path" checkbox.
2.	Get the latest Java from https://www.java.com/download/ and install it.
3.	Get the latest Microsoft Visual C++ and install it.
4.	update pip, setuptools, and wheel with the following command:
python -m pip install --upgrade pip setuptools wheel
5.	After all those steps, install Taurus:
python -m pip install bzt
To uninstall -> pip uninstall bzt
Note: If there is no JMeter installed at the configured path, Taurus will attempt to install the latest JMeter and associated plugins into this location (by default this is: ~/.bzt/jmeter-taurus/bin/jmeter). You can change this setting to your preferred JMeter location (consider putting it into the ~/.bzt-rc file)
default-executor: jmeter

bzt /c/Gatling/uat12_redis_data.jmx(location of your jmeter script)
