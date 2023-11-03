# sdfefsfsd
dwadadstge
But then the discussion evolved and I thought, I'll show you a very minimal example in C. What is the smallest chat server you can write? For starters to be truly minimal we should not require any proper client. Even if not very well, it should work with telnet or nc (netcat). The server main operation is just to receive some chat line and send it to all the other clients, in what is sometimes called a fan-out operation. But yet, this would require a proper readline() function, then buffering, and so forth. We want it simpler: let's cheat using the kernel buffers, and pretending we every time receive a full-formed line from the client (an assumption that is in the practice often true, so things kinda work).

Well, with this tricks we can implement a chat that even has the ability to let the user set their nick in just 200 lines of code (removing spaces and comments, of course). Since I wrote this little program as an example for my friends, I decided to also push it here on Github.



# Created by https://www.toptal.com/developers/gitignore/api/rust,visualstudiocode,clion,dotenv,direnv,linux,macos,windows
# Edit at https://www.toptal.com/developers/gitignore?templates=rust,visualstudiocode,clion,dotenv,direnv,linux,macos,windows

### CLion ###
# Covers JetBrains IDEs: IntelliJ, RubyMine, PhpStorm, AppCode, PyCharm, CLion, Android Studio, WebStorm and Rider
# Reference: https://intellij-support.jetbrains.com/hc/en-us/articles/206544839

# User-specific stuff
.idea/**/workspace.xml
.idea/**/tasks.xml
.idea/**/usage.statistics.xml
.idea/**/dictionaries
.idea/**/shelf

# AWS User-specific
.idea/**/aws.xml

# Generated files
.idea/**/contentModel.xml

# Sensitive or high-churn files
.idea/**/dataSources/
.idea/**/dataSources.ids
.idea/**/dataSources.local.xml
.idea/**/sqlDataSources.xml
.idea/**/dynamic.xml
.idea/**/uiDesigner.xml
.idea/**/dbnavigator.xml

# Gradle
.idea/**/gradle.xml
.idea/**/libraries

# Gradle and Maven with auto-import
# When using Gradle or Maven with auto-import, you should exclude module files,
# since they will be recreated, and may cause churn.  Uncomment if using
# auto-import.
# .idea/artifacts
# .idea/compiler.xml
# .idea/jarRepositories.xml
