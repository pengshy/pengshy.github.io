---
layout: post
title: 二分查找
description: >
  二分查找模板和思路分析
categories: [algorithm]
tags: [binary-search]
sitemap: false
hide_last_modified: true
---

# 二分查找的难点

+ 边界条件的判断：什么时候才能终止循环？

+ 如何避免写出死循环

# 模板

```c++
bool check(...)

void bs(int l, int r)
{
	while (l < r)
	{
		int mid = l + r >> 1;
		if (check(...)) r = mid;
		else l = mid + 1;
	}
}

void bs(int l, int r)
{
	while (l < r)
	{
		int mid = l + r + 1 >> 1;
		if (check(...)) r = mid - 1;
		else l = mid;
	}
} 

PS：这里为了防止越界的问题，mid = l + r >> 1 可以改写为 mid = l + (r - l) / 2
```



