
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate   -DarchetypeGroupId=com.adobe.aem   -DarchetypeArtifactId=aem-project-archetype   -DarchetypeVersion=40   -DappTitle="Geeks Demo"   -DappId="geeksdemo"   -DgroupId="com.geeks.demo"   -DaemVersion=6.5.5   -DsingleCountry=n  -DfrontendModule="react"  


mvn -B archetype:generate   -DarchetypeGroupId=com.adobe.aem   -DarchetypeArtifactId=aem-project-archetype   -DaemVersion=6.5.5   -DfrontendModule=none   -DincludeDispatcherConfig=n   -DarchetypeVersion=25   -DappTitle="My Site"   -DappId="mysite"   -DgroupId="com.mysite" 





// To get the tagManager
final TagManager tagManager = resourceResolver.adaptTo(TagManager.class); 

// To get the tagId
Tag tag = resource.adaptTo(Tag.class); 
String tagId = tag.getTagID();

//To get the tag title
String tagTitle = resource.getValueMap().get("jcr:title", String.class);	

// To get the tag name
String tagName = resource.getName();	


// To read all the tags

@ResourcePath(path="/content/cq:tags/we-retail")
Resource res;


public List<String> getTags() throws RepositoryException {
if (null != res) {
Iterator<Resource> tagList = res.listChildren();
while (tagList.hasNext()) {
Resource tagchildRes = tagList.next();
Tag tag = tagchildRes.adaptTo(Tag.class);
String tagId = tag.getTagID();
String tagName = tagchildRes.getName();
String tagTitle = tagchildRes.getValueMap().get("jcr:title", String.class);
tList.add(tagTitle);
}
session.save();
session.refresh(true);
}
return tList;
}

