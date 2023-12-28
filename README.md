product = []
price = []

size = int(input("enter the size : - "))

for i in range(size):
  i = input("enter the product name : - ")
  product.append(i)

for i in range(size):
  i = input("enter the product price : - ")
  price.append(i)

  print("...............")
  
YES = input('do you want to add GST[Y/N]')

if YES == "Y" or YES == "y" :
    gst = int(input("enter gst "))
    total = 0
    for i in range(size):
       total = total + price[i]
       print((i+1),'.',product[i],'=>',price[i],'/-')
    gstamount = total*gst/100
    mrp = total+gstamount
    print('gst',gst)
    print('gst amount',gstamount)
    print('mrp',mrp)
else :
  total = 0
  for i in range(size):
     total = total + price[i]
     print((i+1),'.',product[i],'=>',price[i],'/-')
  print('................')
  print("total amount without gst",total)
