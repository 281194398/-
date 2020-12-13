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

# class Solution:
#     def reverse(self, x):
#         s = str(x)
#         if s[0] == '-':
#             x = int('-' + s[1:][::-1])
#         else:
#             x = int(s[::-1])
#         return x if -2147483648< x <2147483647 else 0
