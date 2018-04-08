from string import*
s="When I was young I'd listen to the redio"
print("%20d"%(s.count("I")))#get how many times "I" appears
print(s.split(" "))#find the blank and make a cut
print("%21d"%(len(s)))
print(s.startswith("I"))
print(s.replace("redio","radio"))
print(s)
