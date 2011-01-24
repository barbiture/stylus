
## Variable Arguments

 Stylus supports variable-length arguments in the form of `name...`. These arguments consume the remaining arguments passed to a mixin or function. This is useful for example when utilizing the implicit function call support to apply vendor prefixes like `-webkit` or `-moz`.
 

In the example below we consume all the arguments passed and simply apply them to multiple properties.

     box-shadow(args...)
       -webkit-box-shadow args
       -moz-box-shadow args
       box-shadow args

     #login
       box-shadow 1px 2px 5px #eee

yielding:

      #login {
        -webkit-box-shadow: 1px 2px 5px #eee;
        -moz-box-shadow: 1px 2px 5px #eee;
        box-shadow: 1px 2px 5px #eee;
      }
