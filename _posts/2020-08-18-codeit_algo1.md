---
title: Palindrome Algorithm
tags: reivew
---
### 마켓컬리 인사이트 독후감

<div class="message">
 토마토나 기러기처럼 거꾸로 읽어도 똑같은 단어를 팔린드롬(Palindrome)이라고 부른다. 문자열 word가 파린드롬인지 확인하는 함수를 만들어보도록 하겠다. 
</div>

<code>
  def is_palindrome(word):
    for left in range(len(word)//2)
    right = len(word) - left - 1
    if word[left] != word[right]
      return False

    return True
  
  print(is_palindrome("racecar"))
</code>
