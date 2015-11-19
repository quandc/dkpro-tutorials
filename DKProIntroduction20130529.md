# Introduction to DKPro - 2013-05-29 #
This tutorial was held on May 29 by Dr. Judith Eckle-Kohler and Roland Kluge at [DIPF](http://www.dipf.de/en/dipf-news/), Frankfurt in the context of the [PhD program Knowledge Discovery in Scientific Literature](http://www.kdsl.tu-darmstadt.de/de/knowledge-discovery-in-scientific-literature/). It is designed as a one-day tutorial with programming part. The tutorial material has been developed by Dr. Judith Eckle-Kohler, Richard Eckart de Castilho, Roland Kluge, and Dr. Torsten Zesch. The tutorial covers an introduction to the DKPro Java development infrastructure (e.g., Maven, Continuous Integration), UIMA and DKPro-Core.


# Introduction to the Java Development Infrastructure #
> After working through the slides and material listed below, you should be able to answer at least the following questions:
    * What are Maven artifacts and where are they stored?
    * Which Maven repositories do you know? What are the differences between them?
    * Committing a newly created Maven project to SVN: which folders and files should never be commited?
    * When should you create trunk/tags folders for your Maven project?
    * When to create a multi-module Maven project?
    * What is Continuous Integration and when should you consider using it?

## Slides ##

Soon to come

## Step-by-step Instructions ##

Installing Eclipse
  * [Eclipse Installation and Setup](EclipseInstallationAndSetup.md)

Maven Guidelines
  * Connecting to Maven repositories, [UKP Public Maven Repository](http://code.google.com/p/dkpro-core-asl/wiki/UkpMavenRepository)
  * [Creating a Single-Module Project](CreateSingleModuleMavenProject.md)
<a href='Hidden comment: 

* [CreateMultiModuleMavenProject Multi-Module Projects] (when to use, how to create, refactoring)
'></a>

  * [Maven Troubleshooting](MavenTroubleshooting.md)
  * [Dependency Management](MavenDependencyManagement.md)


Version Control SVN Guidelines
  * [Checking a new Maven project into SVN](CheckingInAProject.md)
  * [Synchronizing your workspace](EclipseSynchronizeWorkspace.md)

Java Guidelines

  * [Java Code Conventions](http://www.oracle.com/technetwork/java/codeconv-138413.html)

# Introduction to UIMA #

## Slides ##

[Slides UIMA pdf](https://dkpro-tutorials.googlecode.com/svn/de.tudarmstadt.ukp.dkpro.tutorial/tags/dkprointro20130529/dkproIntroUima.pdf)

## Tutorial Code ##
> Example project UIMA: https://dkpro-tutorials.googlecode.com/svn/de.tudarmstadt.ukp.dkpro.tutorial/trunk/uimaintro/de.tudarmstadt.kdsl.teaching.uimaintro

# Introduction to DKPro Core #
## Slides ##

[Slides DKPro Core pdf](https://dkpro-tutorials.googlecode.com/svn/de.tudarmstadt.ukp.dkpro.tutorial/tags/dkprointro20130529/dkproIntroCore.pdf)

## Tutorial Code ##
> Example project DKPro Core: https://dkpro-tutorials.googlecode.com/svn/de.tudarmstadt.ukp.dkpro.tutorial/trunk/de.tudarmstadt.kdsl.teaching.dkprocore.intro