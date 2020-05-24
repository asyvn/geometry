---
layout: post
title: Thử highlight asy code.
subtitle: 
cover-img:
tags: [asymptote, geometry]
---

```asymptote
pair [] p, m;

real s=abs(a-b)/3;
pair c=n[l-1], d=q[l-1];

for (int i=0; i<=k; ++i){
	m[i]=(a.x+i*s,a.y);
	p[i]=(d.x+i*s,d.y);
	
	if (i % 2==0)  devide(m[i],p[i],(l-1));
	else devide(p[i],m[i],(l-1));
}
```
