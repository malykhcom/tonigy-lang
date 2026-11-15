# tonigy-lang
Tonigy Programming Language

Of course, the Tonigy programming language is statically typed. I don't like dynamically typed languages and try to avoid using them.

One of Tonigy's foundations is a type system independent of Java. I deliberately avoided any direct compatibility between them. Moreover, the way Tonigy's type system is mapped to the JVM may change as the compiler evolves (optimized). There are strict rules for interaction and compatibility at the points where Tonigy code and Java code intersect, but only at those points.

Therefore, a Tonigy library may be packaged as a jar-file, but it contains only a few compiled class files. The remainder is provided as resources, with which the compiler works. This significantly reduces binary compatibility problems as Tonigy evolves.

Additionally, Tonigy's type system deliberately lacks a direct replacement for Object (the single most general class). This makes more efficient type optimizations possible, and does not get in the way in practical programming when generics are present.
