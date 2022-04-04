---
layout: post
title: 9. instance()
date: 2022-04-05 03:39:02+0900
tags: 
# description: >
#   설명
related_posts:
categories:
   - blog
   - python
---

* toc
{:toc .large-only}


```python
isinstance(1, int)
# 1이 int형인지 알아본다. 결과는 True




isinstance("가나다", str)
# "가나다"가 str형인지 알아본다. 결과는 True




lst = [1, 2, 3, 4, 5, [6, 7, 8, 9]]
isinstance(lst, list)
# lst가 list형인지 알아본다. 결과는 True




# lst의 중첩 리스트 요소까지 출력하기
for i in lst:
    if isinstance(i, list):
        for j in i:
            print(j)

    else:
        print(i)

-----
1
2
3
4
5
6
7
8
9
```