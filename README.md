import urllib
import re

site = urllib.urlopen('https://www.msn.com/en-us/news')
html = site.read()
header_tags = re.findall(r'<h[1-2][^>]*><a[^>]*>(.*?)</a></h[1-2]>', str(html))
print str('\n'.join(header_tags)) 
