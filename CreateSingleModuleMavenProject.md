# Directory layout #
  * in the SVN create a folder _NICE\_PROJECT\_NAME_ with subfolders _trunk_, _tags_ and _branches_
  * the subfolders _trunk_ and _tags_ are important prerequisites for
    * making a release with Maven
    * creating a tag in order to freeze a particular version of your experiment project

# Create a Maven Project #

In Eclipse, create a Maven project as described in the DKPro-Core First-Steps Tutorial on Google Code:
  * http://code.google.com/p/dkpro-core-asl/wiki/MyFirstDKProProject#Create_a_project
  * http://code.google.com/p/dkpro-core-asl/wiki/MyFirstDKProProject#Configure_the_POM
    * mind that the Dependency Management pane in Eclipse sometimes does not show artifacts when you try to add them, although they are in the Artifactory
    * in this case, you have to edit the _pom.xml_ source code and add the dependency manually, after looking it up in the Artifactory (e.g. on [zoidberg](https://zoidberg.ukp.informatik.tu-darmstadt.de/artifactory/webapp/home.html))

When you create a new UKP-internal or KDSL-internal Maven project, be sure to use the following **parent POM**, latest version:

```xml

<parent>

<artifactId>de.tudarmstadt.ukp.dkpro.misc.superpom

Unknown end tag for &lt;/artifactId&gt;



<groupId>de.tudarmstadt.ukp.dkpro.misc

Unknown end tag for &lt;/groupId&gt;



<version>...

Unknown end tag for &lt;/version&gt;





Unknown end tag for &lt;/parent&gt;


```

# Check in your project #
Check in your newly created Maven project in the SVN under _NICE\_PROJECT\_NAME/trunk_, see also [CheckingInAProject](CheckingInAProject.md).