# deb Task #

## Task definition in your build file ##
To use the deb task, you will have to define it in your build file. This is done by following code:
```
    <path id="ant-deb.classpath">
        <fileset dir="enterHereYourDirectoryPathTo_ant-deb-{version}.jar" includes="*.jar"/>
    </path>

    <taskdef name="deb" classname="com.googlecode.ant_deb_task.Deb" classpathref="ant-deb.classpath"/>
```

Here you can find the ant-deb-{version}.jar http://code.google.com/p/ant-deb-task/downloads/list

## Attributes ##

  * **debFilenameProperty**
  * **toDir**
  * **package**
  * **version**
  * **section** - one of: ("admin", "base", "comm", "devel", "doc", "editors", "electronics", "embedded", "games", "gnome", "graphics", "hamradio", "interpreters", "kde", "libs", "libdevel", "mail", "math", "misc", "net", "news", "oldlibs", "otherosfs", "perl", "python", "science", "shells", "sound", "tex", "text", "utils", "web", "x11") and also the following prefixes could be used: ("contrib/", "non-free/")
  * **priority** - one of: ("required", "important", "standard", "optional", "extra")
  * **architecture**
  * **depends**
  * **preDepends**
  * **recommends**
  * **suggests**
  * **enhances**
  * **conflicts**
  * **provides**
  * **maintainer**
  * **homepage**
  * **preinst**
  * **postinst**
  * **prerm**
  * **postrm**
  * **config**
  * **templates**

## Nested Elements ##

  * **description**
    * **synopsis**
    * extended description as text
  * **version**
    * **epoch**
    * **upstream**
    * **debian**
  * **maintainer**
    * **name**
    * **email**
  * **conffiles**
    * tafileset of conffiles
  * one or more tarfileset

## Examples ##
Some examples are provided in examples-{version}.tar.gz at http://code.google.com/p/ant-deb-task/downloads/list