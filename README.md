# OptimusId

Id obfuscation based on Knuth's multiplicative Hashing Algorithm for Elixir. This library lets you obfuscate numerical identifiers via reversible mapping. For example you can encode  your customers ids so that they can be safely exposed in a url and when needed internal map them back to their original value.

For more info see: https://gist.github.com/badboy/6267743


 Add OptimusId as a dependency to your Mix project:
 
 ```elixir
defp deps do
  [{:optimus_id, "~> 1.0"}]
end
```
 
OptimusId encodes an integers into a new integer based on:

 * Large prime number lower than 2147483647
 * The inverse prime so that (PRIME * INVERSE) & MAXID == 1
 * A large random integer lower than 2147483647


s = OptimusId.new(1580030173, 59260789, 1163945558)

OptimusId.encode(s, 20)
#=> 1535832388

OptimusId.encode(s, 1535832388)
#=> 20


