# 20211005

#1대문자 소문자 판별

def solution(random_char):
  ascii_char = ord(random_char)
  if ascii_char >= 65 and ascii_char <= 90:
    return 1
  elif ascii_char >= 97 and ascii_char <= 122:
    return 0
  else: 
    return -1
    
    
#2대문자 소문자 변환

def solution(random_char):
  ascii_char = ord(random_char)
  diff_char = ord('a') - ord('A')
  if ascii_char >= 65 and ascii_char <= 90:
    return chr(ascii_char+diff_char)
  elif ascii_char >= 97 and ascii_char <= 122:
    return chr(ascii_char-diff_char)
  else:
    return random_char

#3 최대와 최소 사이


def get_min(a, b, c):
  min_value = 2**64-1
  if a >= b:
    min_value = b
  else:
    min_value = a
  if min_value >= c:
    min_value = c
  return min_value
  
def get_max(a, b, c):
  max_value = -(2**64)+1
  if a >= b:
    max_value = a
  else: 
    max_value = b
  if max_value <= c:
    max_value = c
  return max_value 

def solution(a, b, c):
  min_value = get_min(a, b, c)
  max_value = get_max(a, b, c)
  if min_value == max_value:
    return -1
  else:
    return max_value - min_value

