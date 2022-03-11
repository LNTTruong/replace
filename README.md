# replacelist = ['4.txt','2.txt','3.txt']
logpath = 'log.txt'

target = input("Nhập vào nội dung cần thay thế: ")
Replace = input("Nhập vào nội dung thay thế: ")
def replace(target,Replace,filepath,logpath):
    f = open(filepath,'r',encoding="utf-8").read().split('\n')
    log = ""
    text=""
    for i in range(0,len(f)):
        if target in f[i]:
            z = f[i].replace(target,Replace)
            text+=z+"\n"
            log+=filepath+" : "+"Line: "+str(i+1)+"\n"
        else:
            text+=f[i]+"\n"
    open(logpath,'a').write(log+"\n")
    open(filepath,'w',encoding="utf-8").write(text)
for i in list:
    replace(target,Replace,i,logpath)
    print("File {0} done!".format(i))
