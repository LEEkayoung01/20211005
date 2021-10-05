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

#3 
