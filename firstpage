from bs4 import BeautifulSoup
import urllib3

#store the location of the html file
page = open('webpage.html', 'r')

soup = BeautifulSoup(page, "html.parser")

find = soup.find_all('a', attrs={'class': 'jobtitle turnstileLink'})

#create list to store what is found in
dump = []


for div in soup.findAll('div', attrs={'class':'row result clickcard'}):
    # print(div.find('a').contents[0])
    dump.append(div.find('a').contents[0])

#second for loop to detect divs that for some reason have a different class. They're the 'sponsored' listings


for div in soup.findAll('div', attrs={'class':'row sjlast result clickcard'}):
    # print(div.find('a').contents[0])
    dump.append(div.find('a').contents[0])

print(dump)

