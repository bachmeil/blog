# Updating Fossil on Ubuntu

My preferred version control system is Fossil. I like the features it provides out of the box relative to Git - it's a pain to add the overhead of installing/maintaining additional functionality that you get for free with Fossil.

This post explains how I keep my Fossil executable in sync with the latest released version. Although having the latest and greatest is not always the goal when you're running a server, Fossil updates tend to be rock solid, so there's no reason to not take advantage of the latest features.

My server is running Ubuntu 18.04. I update using the `checkinstall` utility. If it's not already on your system, install it:

```
apt install checkinstall
```

Download the source code of the latest release:

```
wget [link].tar.gz
```

where `[link]` is replaced by the link taken from the [downloads page](https://fossil-scm.org/home/uv/download.html). As of this writing, the full command is `wget https://fossil-scm.org/home/uv/fossil-src-2.10.tar.gz`. In what follows, I'll assume you're installing version 2.10, but you'll need to update the version appropriately if you're installing a different version.

Extract and enter the directory:

```
tar -xvf fossil-src-2.10.tar.gz
cd fossil-2.10/
```

Configure and build. I prefer to enable the JSON API, so I add that option to the configure step:

```
./configure --json
make
```

The first time I did this, the configure step failed because of a missing zlib. I installed it using:

```
apt install zlib1g-dev
```

Depending on your system, the configure step might fail for other reasons; you'll have to handle dependencies as needed. `build-dep` should also work for this, but I install the needed development libraries manually when I'm compiling my own software.

If it builds without problems, you can test your new fossil executable:

```
./fossil version
```

If that prints out the version you expect, the last step is to remove your existing fossil installation, create a package (specific to your system, not one you'll want to distribute) and install it using your package manager:

```
checkinstall
```

Technically, you could do `make install` rather that `checkinstall`, but then fossil is not part of your package management system. I'm not comfortable with that.

Now it's time to confirm that you can access your repos. One gotcha I encountered the first time I did this was that I installed Fossil using the repo (it was the latest release at that time) but checkinstall puts it in a different directory. You may need to change your CGI config file so that it looks in the right place. I had to change `#! /usr/bin/fossil` to `#! /usr/local/bin/fossil`.