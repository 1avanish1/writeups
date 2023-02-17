# pixelated

using the pillow library from python,we had to individually,
take the RGB values and stack images by adding the pixel value.
```python
rom PIL import Image
 
img1 = Image.open(r"scrambled1.png")
  
# Opening the secondary image (overlay image)
img2 = Image.open(r"scrambled2.png")

p1 = img1.load()
p2 = img2.load()
flag = Image.new("RGB",img1.size)
flagpix = flag.load()
 
for row in range(img1.size[1]) :
    for col in range(img1.size[0]):
        flagpix[col,row] = (
           ( p1[col,row][0]+p2[col,row][0])%256,
            ( p1[col,row][1]+p2[col,row][1])%256,
             ( p1[col,row][2]+p2[col,row][2])%256,
        )
flag.save("flag.png")



```
it runs through the rows and columns  and hence pixel by pixel adds the RGB
values and stores it in the tuple.
