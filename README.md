# python3_tutorial_file


# Use the file name mbox-short.txt as the file name
add = 0
count = 0

fname = input("Enter file name: ")      # The user is promted for a file name
fh = open(fname)                        # 'fname' is opened with the fh handle
for line in fh:                         # Here I establish a for loop
    if not line.startswith("X-DSPAM-Confidence:") : continue            #If it doesn't start with X-DSPAM-Conf..., then I don't want it
#    pos = line.find(':') ,   it's 18   #Needed to establish where the ":" is so i cna get the numbers that follow
    slc = line[19:]                     # Position 19 is after the ":" , and I sliced out the stuff from 19 and on (the numbers)

    flt = float(slc)                    #I have to convert the string of numbers to a float
#now to try and sum the numbers in flt

for value in [flt]:                     # Here I try to sum the numbers but fail. 
    count = count + 1                   # For loops are for sequences and I don't have a sequence, so no for loop needed. So what to use?
    add = add + value


print(count, add)

#print("Average spam confidence:", add)
