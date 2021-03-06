# Texton-Map-Generation-

<p> This code tests for an exact zero difference when we compare two images (Image1, Image2), i.e, Image, 'Image1',
 with a 180 degree rotated version of itself, 'Image2'. TM2, TM1 are the texton Maps generated for these images(Image1, Image2) where the texton map is flipped as well. The file tm.txt stores all the image values, texton Map values and the difference between the two texton maps. The file FR.txt gives the filter responses for every training and testing image. </p>
 
Run instructions:
<ol>
<li>cmake .</li>
<li>make</li>
<li>./textonMap FLAG k N</li>
</ol>
<br> FLAG: 1 - to compute kmeans centers, 0 - to generate texton map
<br> k: no of dictionary words,
<br> N: Num of training images to use (here between 1 and 50) <br>
<em> <strong>Note: </strong>The folder in which training images are stored must be in "example_roads/im%d.jpg" format where %d varies from 1 to N(or less than N, but not more), given above</em>
<br>

<ol> <strong>Points to remember</strong>
<li> To change the number of training images, the folder name: In <em>TextonMapGeneration.cpp</em>, look for <strong>iter</strong> to change the number of training images </li>
<li> To change the folder name: In <em>TextonMapGeneration.cpp</em>, look for <strong>fname</strong> to change the path name and image name format, but they have to have naming that increments by 1</li>
<li> To change testing image: In <em>TextonMapGeneration.cpp</em>, look for <strong>test_image_</strong> and change the file to be read accordingly</li>
<li> To change filter size: In <em>include/filters.hpp</em>, look for <strong>SUP</strong> and change the size accordingly (note: if you change the filter size, kmeans has to be recomputed with that filter size for correct results. Also, if you change the number of kcenters for testing, make sure to compute the kcenters before generating the texton map. </li>
</ol>
