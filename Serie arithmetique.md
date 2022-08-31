---
tags: [concept, math] 
---
# Arithmetic series formula proof
Created: 2022-08-31

Let $d$ be the common difference, $a$ the first term of the sequence and $n$ the number of terms.
	
So when we know $n$, $a (u_1)$, and $d$:

$$S_{n}=d\left(\frac{n(n+1)}{2}\right)+n(a-d)$$
$$S_{n}=\frac{dn(n+1)}{2}+n(a-d)$$
$$S_{n}=\frac{dn(n+1)+2n(a-d)}{2}$$
$$S_{n}=\frac{n[d(n+1)+2(a-d)]}{2}$$
$$S_{n}=\frac{n(d(n+1)+2a-2d)}{2}$$
$$S_{n}=\frac{n(d(n+1-2)+2a)}{2}$$
$$S_{n}=\frac{n(d(n-1)+2a)}{2}$$
$$S_{n}=\frac{n}{2}(d(n-1)+2a)$$
$$S_{n}=\frac{n}{2}(2a+(n-1)d)$$
***
So when we know $n$, $a(u_1)$, and $u_n$:

$$S_{n}=d\left(\frac{n(n+1)}{2}\right)+n(a-d)$$
$$S_{n}=\frac{dn(n+1)}{2}+n(a-d)$$
$$S_{n}=\frac{dn(n+1)+2n(a-d)}{2}$$
$$S_{n}=\frac{dn^2+dn+2an-2dn}{2}$$
$$S_{n}=\frac{dn^2-dn+2an}{2}$$
$$S_{n}=\frac{n(dn-d+2a)}{2}$$
$$S_{n}=\frac{n(dn-d+a+a)}{2}$$
$$S_{n}=\frac{n(dn-d+a+u_1)}{2}$$
$$S_{n}=\frac{n(dn-d+u_1+u_1)}{2}$$
$$S_{n}=\frac{n(d(n-1)+u_1+u_1)}{2}$$
$$S_{n}=\frac{n(d(n-1)+u_1+u_1)}{2}$$
$$S_{n}=\frac{n(u_n+u_1)}{2}$$
$$S_{n}=\frac{n}{2}(u_1+u_n)$$
