# hash
output=''
print 'Enter input (after 100 will be cut out and not over 1000)'
data=raw_input()
data=data.split()
if len(data)>100:
   data=data[:100]
lenght=len(data)
ans=['']*50
for i in range(0,lenght):
    if (int(data[i])<=1000):
        x=int(data[i])%50
        ans[x]+=(data[i]+' ')
for i in range(0,50):
    ans[i]=ans[i].split()
    for j in range(0,len(ans[i])):
        [ ans[i].pop(k) for k in range(len(ans[i]))[::-1] if ans[i].count(ans[i][k]) > 1 ]
    ans[i] = map(int, ans[i])
    print i,':',('\t'.join(map(str, ans[i])))


    
    
