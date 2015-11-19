# Check-in process for new projects #

This document explains how to check a **new experiment** into a SVN repository using Eclipse. We assume that you have an SVN repository that you want to commit to.  If you already have an (empty) project under version control, you may be interested in how to [check single files into an existing project](EclipseSynchronize.md).

The remote address of the SVN repository is denoted with  _SVN\_URL_ here. Further, we suppose that you want to version your project in the subdirectory _experiments_.

  1. **Create a Project** If you haven't already created your project, create as you normally would.  Normally this would be via _File -> New -> Other… -> Maven -> Maven Project_.
Choose reasonable values for Group Id and Artifact Id (should be all lower-case); in the following we use the following value for both Group and Artifact Id: `de.tudarmstadt.ukp.experiments.YOURINITIALS.EXPERIMENTNAME`.
  1. **Register SVN URL** Open the _SVN Repository Exploring_ perspective. If you don't see an entry for _SVN\_URL_, then add it by right clicking on the list and selecting _New -> Repository location…_.
  1. **Share Project** Go back to the Package Explorer of the Java perspective. Right-click on your project and select _Team -> Share project… -> SVN -> Next -> Use existing repository location ->_ SVN\_URL _->Next_.
  1. **Configure path for SVN** A "Share Project" dialog will appear.  Select the "Use specified folder name" radio button and enter the following into the text box: _experiments/YOURINITIALS/EXPERIMENTNAME/trunk/de.tudarmstadt.ukp.experiments.YOURINITIALS.EXPERIMENTNAME_ (again all lower-case).
  1. Click on _Finish_.  You will be taken to the _Team Synchronizing_ perspective.  Don't commit anything here yet and close the _Team Synchronizing_ perspective!
  1. **Ignore locale Eclipse settings** Go back to the Package Explorer of the Java perspective and expand your project. Select the _.settings_ folder and the _.project_ and _.classpath_ files; also select the _target_ folder if it is also marked as under version control. Then right-click and select _Team -> Add to svn:ignore… ->_ Confirm match by filename. _OK_
  1. **Commit your Project** Right click on your project and select _Team -> Commit… ->_ and type your initial commit message. _OK_

# What you should not commit to SVN #

## Checking in a newly created Maven project ##
  * never commit the folders _target_, _.settings_ and the files _.project_ and _.classpath_ to a repository
  * set them to svn:ignore

## Large corpora and lexical resources ##
  * Large corpora and large lexical resources should be stored outside the workspace (e.g., lexical resources might be kept in a database).
  * Never commit corpora or other large resources (anything larger than a typical source code file is considered large) to a repository.

## Resources used for testing ##

Any resources that were explicitly created for a test case should be minimal.

As rules of thumb the following types of resources for testing should not go into SVN, but be packaged as Jar files
  * any resources that were not explicitly created for a test case
  * any binaries
  * any resources that some third party created
  * anything that is generated (this also wouldn't be packaged as a JAR, just be generated during the build)

As always, there are exceptions to the rule, e.g.:

  * JCas wrappers - these are generated, but we have some that contain custom modifications
  * images - when building a web application (does not apply to DKPro Core)