# Compound Statements

Compound statements are made up of other statements, including simple statements. They are composed of something with call *clauses*, which are divided into a *header* and a *suite*. The suite is always indented after the header.

```Python
header line:
	suite
header line:
	suite
```

The *if* statement is an example of a compound statement. Headers can also act like suites if they are nested within other headers.

## Conditional Expressions

Conditional expressions are part of a program statement which specifically evaluates to *True* or *False*. Conditional operators can be expressed in terms of relational operators, as well as boolean operators.

Conditional statements are made up of 3 clauses: if, elif, else.

Whenever a clause is evaluated to true, the other clauses are no longer evaluated. The else clause is only evaluated if all preceding if and elif expressions evaluate to false.

Order matters in conditional expressions this is extra important when their conditions are not mutually exclusive, since two or more statements could be true. Only the first true statement will be evaluated.

Conditional statements can be nested. As soon as the first clause is evaluated to true, it can then start evaluating any conditional statements inside the header.