class Solution(object):
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        target = str(x)
        if target[0] == '-':
            target = target[:0:-1]
            shuzi = int('-' + target)
        else:
            shuzi = int(target[::-1])
        return shuzi if -2**31 <= shuzi <= 2**31 - 1 else 0
        
class Solution(object):
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        a = str(x)
        y = list(a)
        y.reverse()
        if y[-1] == "-":
            y.remove('-')
            y.insert(0, '-')
        y2 = ''.join(y)
        z = int(str(y2))
        if z < (-2**31) or z > (2**31-1):
            z = 0
        return z
        
class Solution(object):
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        xxx  = str(x)
        x = (-1 if xxx.startswith("-") else 1) * int(xxx.lstrip('-')[::-1])

        xx = x >> 30
        if -2 <= xx <= 1:
            return x
        else:
            return 0


# class Solution:
#     def reverse(self, x):
#         s = str(x)
#         if s[0] == '-':
#             x = int('-' + s[1:][::-1])
#         else:
#             x = int(s[::-1])
#         return x if -2147483648< x <2147483647 else 0
