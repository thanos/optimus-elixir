# OptimusElixir

Id obfuscation based on Knuth's multiplicative Hashing Algorithm for Elixir. This library can be used to encode primary keys, for example of your customers, so that the numbers can be safely exposed, such as in a url.

For more info see: https://gist.github.com/badboy/6267743

What you will need is:

 * Large prime number lower than 2147483647
 * The inverse prime so that (PRIME * INVERSE) & MAXID == 1
 * A large random integer lower than 2147483647
 
 
 Add to your `mix.ex` file: 
 
 ```{:optimus_elixir, "~> 2.0"}```
 
 
 
