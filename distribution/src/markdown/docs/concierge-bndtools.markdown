## Running Concierge with Bnd(tools)

[Bnd](http://www.aqute.biz/Bnd/Bnd) is one of the most popular tools for developing OSGi bundles.
It provides tooling for easily creating the required OSGi Manifest headers, and much more.
[Bndtools](http://www.bndtools.org) is a popular Eclipse plugin based on Bnd that provides integration
with the Eclipse IDE for developing OSGi bundles.

Bnd also provides a means for writing launch configurations to launch an OSGi runtime with a set
of bundles and properties in the form of a .bndrun file. In order to use Concierge with the Bnd launching mechanism, first make sure that the org.eclipse.concierge .jar is available in the repository. An easy way to accomplish this is to drop the .jar in your project workspace's local repository. Then you can easily use Concierge by setting `-runfw` to concierge in your .bndrun file:

```
-runfw: org.eclipse.concierge
```

When you now launch your .bndrun file, it will automatically use Concierge as OSGi framework.
