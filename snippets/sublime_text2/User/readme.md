Todo:
---
* finish grammar syntax definition
* prepare colour scheme
* think about code folding - should it be only for branching structures only?


Problems:
---
* it seems that there's no easy way to extend _current_ sublime text colour scheme, so we have to do the following: when the package is being installed, find the current colour scheme path and apply our scheme as a patch to it (if it doesn't already have corresponding schemes - can look up by scopes)
* as there's no simple way to determine if current template is not included for every loop iteration of some parent template, should we consider highlighting dot-prefixed vars as invalid if they are used not within a loop?
* how should we update the list of available functions? Just manually?

Rules:
---

**Variables**:

* referencing a variable by wrapping its name in double dash returns the value of the variable
* when a variable name is prefixed with . (dot), the variable name will be looked up in the current iterating array

**Expressions**:

* simple expressions can be just wrapped in ## (double dash) - SetVars, GetCookie, Inc, Mod, and others
* complex expressions can be wrapped 


Andrey already did something for this: https://github.com/apleshkov/mailru-tmpl-intellij-plugin/blob/master/src/com/mailru/plugins/thtml/lang/lexer/thtml.flex