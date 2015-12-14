# hash
output=''
print 'Enter input (after 100 will be cut out)'
data=raw_input()
data=data.split()
if len(data)>100:
   data=data[:100]
lenght=len(data)
i=0
ans=['']*50
for i in range(0,lenght):
    x=int(data[i])%50
    ans[x]+=(data[i]+' ')
    
    
    
