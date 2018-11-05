# OptimusId

Id obfuscation based on Knuth's multiplicative Hashing Algorithm for Elixir. This library lets you obfuscate numerical identifiers via reversible mapping. For example you can encode  your customers ids so that they can be safely exposed in a url and when needed internal map them back to their original value.

For more info see: https://gist.github.com/badboy/6267743

What you will need is:

 * Large prime number lower than 2147483647
 * The inverse prime so that (PRIME * INVERSE) & MAXID == 1
 * A large random integer lower than 2147483647
 
 
 Add OptimusId to your `mix.ex` file: 
 
 ```Add Hashids as a dependency to your Mix project:

defp deps do
  [{:optimus_id, "~> 1.0"}]
end```
 
 
 
