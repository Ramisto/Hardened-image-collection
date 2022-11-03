# Hardened-image-collection

##### Security from the design of an application is essential, and saves everyone time.

##### This collection of images will allow you to easily deploy security recommendations.

## Referential
### CIS
The Center for Internet Security (CIS) is anonprofit organization, formed in October, 2000. Its mission is to make the connected world a safer place by developing, validating, and promoting timely best practice solutions that help people, businesses, and governments protect themselves against pervasive cyber threats. The organization is headquartered in East Greenbush, New York, with members including large corporations, government agencies, and academic institutions. (Wikipedia)

The	following	configuration	profiles	are	defined	by	this	Benchmark:

##### Level	1
Items	in	this	profile	intend	to:
  - be	practical	and	prudent;
  - provide	a	clear	security	benefit;	and
  - not	inhibit	the	utility	of	the	technology	beyond	acceptable	means.
##### Level	2
This	profile	extends	the	"Level	1"	profile.	Items	in	this	profile	exhibit	one	or	more	of	
the	following	characteristics:
  - are	intended	for	environments	or	use	cases	where	security	is	paramount
  - acts	as	defense	in	depth	measure
  - may	negatively	inhibit	the	utility	or	performance	of	the	technology.

## Use

``` 
docker build -t CIS/Level1/alpine-apache/Dockerfile .
```
