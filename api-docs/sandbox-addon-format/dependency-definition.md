# Dependency Definition

{% tabs %}
{% tab title="Simple" %}
Below are examples of some common use cases, as well as syntactic sugar

* Wildcard Ranges \(`*`\|`X`\|`x`\) - `1.*` which is equivalent to `>=1.0.0 & <2.0.0`
* Tilde Ranges \(`~`\) - `~1.5` which is equivalent to `>=1.5.0 & <1.6.0`
* Hyphen Ranges \(`-`\) - `1.0-2.0` which is equivalent to `>=1.0.0 & <=2.0.0`
* Caret Ranges \(`^`\) - `^0.2.3` which is equivalent to `>=0.2.3 & <0.3.0`
* Partial Version Ranges - `1` which is equivalent to `1.X` or `>=1.0.0 & <2.0.0`
* Negation operator - `!(1.x)` which is equivalent to `<1.0.0 & >=2.0.0`
* Parenthesized expressions - `~1.3 | (1.4.* & !=1.4.5) | ~2`
{% endtab %}

{% tab title="BNF Grammar" %}
```text
          <semver-expr> ::= "(" <semver-expr> ")"
                          | "!" "(" <semver-expr> ")"
                          | <semver-expr> <more-expr>
                          | <range>

            <more-expr> ::= <boolean-op> <semver-expr>
                          | epsilon

           <boolean-op> ::= "&" | "|"

                <range> ::= <comparison-range>
                          | <wildcard-range>
                          | <tilde-range>
                          | <caret-range>
                          | <hyphen-range>
                          | <partial-version-range>

     <comparison-range> ::= <comparison-op> <version> 
                          | <version>

       <wildcard-range> ::= <wildcard>
                          | <major> "." <wildcard>
                          | <major> "." <minor> "." <wildcard>

          <tilde-range> ::= "~" <version>

          <caret-range> ::= "^" <version>

         <hyphen-range> ::= <version> "-" <version>

<partial-version-range> ::= <major>
                          | <major> "." <minor>

              <version> ::= <major>
                          | <major> "." <minor>
                          | <major> "." <minor> "." <patch>

        <comparison-op> ::= "=" | "!=" | ">" | ">=" | "<" | "<="

                <major> ::= <numeric-identifier>

                <minor> ::= <numeric-identifier>

                <patch> ::= <numeric-identifier>

   <numeric-identifier> ::= "0"
                          | <positive-digit>
                          | <positive-digit> <numeric-identifier>

       <positive-digit> ::= "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"

             <wildcard> ::= "*" | "x" | "X"
```
{% endtab %}
{% endtabs %}

