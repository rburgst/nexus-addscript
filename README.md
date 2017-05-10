# nexus-addscript

This is a nexus upload script that can upload groovy scripts into nexus 3.

This project basically copies the sample nexus groovy upload script and packages it in a fat jar, 
so that it can be used in docker containers, etc where downloading all dependencies is not encouraged.

For more info, please check

* [https://github.com/sonatype/nexus-book-examples/blob/nexus-3.x/scripting/complex-script/addUpdateScript.groovy](https://github.com/sonatype/nexus-book-examples/blob/nexus-3.x/scripting/complex-script/addUpdateScript.groovy)


## Build

	gradle shadowJar
	
## Usage

	java -jar build/libs/nexus-addscript-all.jar -u "admin" -p "admin123" -n "config" -f "./config.groovy" -h "http://localhost:8081"