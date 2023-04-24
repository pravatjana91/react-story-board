
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate   -DarchetypeGroupId=com.adobe.aem   -DarchetypeArtifactId=aem-project-archetype   -DarchetypeVersion=40   -DappTitle="Geeks Demo"   -DappId="geeksdemo"   -DgroupId="com.geeks.demo"   -DaemVersion=6.5.5   -DsingleCountry=n  -DfrontendModule="react"  


mvn -B archetype:generate   -DarchetypeGroupId=com.adobe.aem   -DarchetypeArtifactId=aem-project-archetype   -DaemVersion=6.5.5   -DfrontendModule=none   -DincludeDispatcherConfig=n   -DarchetypeVersion=25   -DappTitle="My Site"   -DappId="mysite"   -DgroupId="com.mysite" 

