---
layout: post
title: Sử dụng barycentric coordinate.
subtitle: 
cover-img:
tags: [asymptote, barycentric]
---

Sử dụng **barycentric coordinate** để viết hàm liên quan đến tam giác được gọn gàng hơn. Sau đây là ví dụ về hàm xác định **tâm nội tiếp**, và **tâm ngoại tiếp** của 3 điểm A, B, C:

```Asymptote    
pair incenter(pair A, pair B, pair C){
	real a=abs(B-C), b=abs(C-A), c=abs(A-B);
	return (a*A + b*B +c*C)/(a+b+c);
}

pair center3p(pair A, pair B, pair C){
	real a=abs(B-C), b=abs(C-A), c=abs(A-B);
	real alpha = acos((b^2 + c^2 - a^2)/(2*b*c)), beta = acos((c^2 + a^2 - b^2)/(2*c*a)), gamma = acos((a^2 + b^2 - c^2)/(2*a*b));
	
	return (sin(2alpha)*A + sin(2beta)*B + sin(2gamma)*C)/(sin(2alpha) + sin(2beta) + sin(2gamma));
}
```
