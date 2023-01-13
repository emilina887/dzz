result = []


def divider(a, b):
    try:
        a / b
    except ZeroDivisionError:
        print('division by zero')
    finally:
        if type(a) == str:
            a = int(a)
    if a < b:
        try:
            a = a + b
        except ValueError:
            print('a < b')
    if b > 100:
        raise IndexError
    return a / b


data = {10: 2, 2: 5, "123": 4, 18: 0, []: 15, 8: 4}
for key in data:
    res = divider(key, data[key])
    result.append(res)

print(result)
