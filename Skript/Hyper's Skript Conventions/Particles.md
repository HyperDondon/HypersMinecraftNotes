# Dust particles
Please for the love of God: 

Do NOT use the ```extra``` value for ```dust``` or ```dust transition``` particles, or any particles that don't use this value. 

I've seen things like:
```vb
make 1 of dust using dustOption(red, 1) at {_loc} with extra 0.000001
```
This makes me cry. 

It does nothing but cause confusion. 

# Vectors
For vectors, avoid using the ```[the] vector (from|between) %location% (to|and) %location%``` [syntax](https://skripthub.net/docs/?id=874). 

Use it if you need to. But don't use these for expanding circles. It can get confusing and complex (trust me). 
