<img src="https://www.polystat.org/logo.svg" height="92px"/>

[![EO principles respected here](https://www.elegantobjects.org/badge.svg)](https://www.elegantobjects.org)
[![DevOps By Rultor.com](http://www.rultor.com/b/polystat/polystat)](http://www.rultor.com/p/polystat/polystat)
[![We recommend IntelliJ IDEA](https://www.elegantobjects.org/intellij-idea.svg)](https://www.jetbrains.com/idea/)

[![CI checks](https://github.com/polystat/polystat/actions/workflows/mvn.yml/badge.svg)](https://github.com/polystat/polystat/actions/workflows/mvn.yml)
[![PDD status](http://www.0pdd.com/svg?name=polystat/polystat)](http://www.0pdd.com/p?name=polystat/polystat)
[![codecov](https://codecov.io/gh/polystat/polystat/branch/master/graph/badge.svg)](https://codecov.io/gh/polystat/polystat)

[![Javadoc](http://www.javadoc.io/badge/org.polystat/polystat.svg)](http://www.javadoc.io/doc/org.polystat/polystat)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/polystat/polystat/blob/master/LICENSE.txt)
[![Maven Central](https://img.shields.io/maven-central/v/org.polystat/polystat.svg)](https://maven-badges.herokuapp.com/maven-central/org.polystat/polystat)
[![Hits-of-Code](https://hitsofcode.com/github/polystat/polystat)](https://hitsofcode.com/view/github/polystat/polystat)
![Lines of code](https://img.shields.io/tokei/lines/github/polystat/polystat)

This is an experimental polystat static analyzer.

Read the [White Paper](https://www.polystat.org/wp.pdf) first.

Download `polystat-*-jar-with-dependencies.jar` 
from [Maven Central](https://search.maven.org/artifact/org.polystat/polystat) 
and then run (replace the asterisk with the 
[latest version](https://repo.maven.apache.org/maven2/org/polystat/polystat/)):

```bash
$ java -jar polystat-*-jar-with-dependencies.jar src temp
```

The `src/test.eo` file must contain the code in [EOLANG](https://www.eolang.org)
with a single object named `test`.
For example, try this simple program that has a "division by zero" bug:

```
[x] > test
  div. > @
    42
    x
```

The output of Polystat will show you which values of `x` may cause
this program to crash. A new directory `temp/` will be created
automatically and will contain temporary files.

You can also play with it by editing the files in `sandbox/`
and then running `./try.sh`.
