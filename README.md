# Happy-number-beautiful-number
python code of Happy number / beautiful number

def happynumber(n):
    def square_sum_digits(num):
        total=0
        while num>0:
            digit = num%10
            print("digit is: ",digit)
            total += digit**2
            print("total is: ",total)
            num //= 10
            print("num is: ",num)
        return total
    seen=set()
    while n!=1 and n not in seen:
        seen.add(n)
        n=square_sum_digits(n)
    print("Seen set is: ",seen)
    print("new n is: ",n)
    return n==1
num=int(input("enter a number: "))
if happynumber(num):
    print("1")
else:
    print("0")
