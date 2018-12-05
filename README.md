# ANTLR4 Calculator Example
ANTLR4 calculator example and explanation

# How do I set this up?
* Install packages using Maven (see `pom.xml`)
* This automatically generates
 the required classes through ANTLR4
* For manually updating/regenerating the required classes
 based on the grammar, you can let Maven execute the
 antlr4:antlr4 command

# What is going on?
ANTLR4 generates Parser, Visitor and Listener
classes based on the `Calculator.g4` grammar
found in `src/main/antlr4/parser`.
These classes contain context and methods needed
for visiting the nodes in the parse tree or
for listening to events when entering or exiting
the nodes in a parse tree.
In this example, a Visitor approach has been used.

The `CalculationVisitor` is a custom class that extends
the base visitor generated by ANTLR4. In this custom class,
we can overwrite the steps taken when visiting each node
in a certain expression.

# Where are all the classes?
ANTLR4 generates these class files
in the target directory. You can use the
maven commands defined in the `pom.xml`.

# Author
Alex Rothuis: [@arothuis](https://twitter.com/arothuis)

[arothuis.nl](arothuis.nl)
