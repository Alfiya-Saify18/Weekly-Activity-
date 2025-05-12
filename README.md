def elevatorstory(F):
    rings=0 #variable for no of rings
    wait=0   #variable for no of waits
    timetomove=F*2
    for i in range(1,F+1):
        if i%4==0:
            rings+=2
        elif i%2==1:
            rings+=1
        if i%4==0 and i%7==0:
            continue
        elif i%7==0:
            wait+=1
    totaltime=timetomove+wait*5
    return {"Rings":rings,"Wait":wait,"Total time in seconds":totaltime}
print(elevatorstory(30))

