FROM ubuntu

RUN apt-get update && apt-get install -y python3

CMD ["python3", "-c", "\
def isHappy(n):\n\
    cycle = []\n\
\n\
    while n != 1:\n\
        count = 0\n\
        for x in cycle:\n\
            if x == n:\n\
                count += 1\n\
            if count == 2:\n\
                return False\n\
\n\
        sum = 0\n\
\n\
        while n > 0:\n\
            digit = n % 10\n\
            sum += digit * digit\n\
            n = n // 10\n\
\n\
        n = sum\n\
        cycle.append(n)\n\
\n\
    return True\n\
\n\
print(isHappy(19))\n\
print(isHappy(2))\
"]