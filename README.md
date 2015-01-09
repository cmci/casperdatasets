# Casperdatasets

## Deployment

Building casperdatasets is a bit tricky. The 'casperdatasets' artifact
must be built with Maven 2.2.0, and Java 1.5. (The source version is
set to 1.4, but Maven will not work with Java 1.4.) See the repository
above for details. (Note the use of the 'ics_deploy' branch.)

Building the casperdatasets-io and casperdatasets-ext artifacts,
though, both of which are contained in the capserdatasets repo, should
be done with a modern Java/Maven combo. (I used openjdk 1.7.0_71 and
Maven 3.0.5.)

Note that java's path was left hard-coded in the casperdatasets
artifact pom.xml, simply because it didn't work immediately when I
tried to change that. Unless you're installing your jdk in
/opt/jdk1.5.0_22, you'll need to edit that by hand.

None of the other modules are currently set up to compile correctly or
deploy to Infochimps' repositories.

You'll also need your settings.xml set up with the credentials
necessary to deploy to Infochimps' parent repository. See instructions
for setting this up in
https://github.com/infochimps-platform/parent-pom

If you set things up correctly, deploying to Infochimps' repositories
should just be a matter of running `mvn deploy` in each of the
following directories:

- casperdatsets
- casperdatsets-io
- casperdatsets-ext
