---
layout: post
title:  "Internship Experience: NVIDIA-HARVARD, Deep Learning Engineering Intern"
date:   2017-05-25 07:52:31 +0530
categories: jekyll update
comments: true
author: Nikhil Wani | ~5 mins read

---

<style type="text/css">

.image
{

 float:left;
 margin-top: 6px;
 margin-right: 7px;
 margin-bottom: -7px;  
 height: 100px;
 border: 5px;
 border-radius: 5px;
}

body
{
	text-align: justify;
}

</style>

![image info](/imgs/cnn-architecture.png)

`TASK:` Brain Tumor Segmentation

`DATASET:`
<!-- <a href="http://www.twitter.com/shawtyanswers" target="_blank"><img src="/imgs/shawtyanswers.jpg" alt="Swaty's Image" class="image"></a>
<a href="http://www.twitter.com/shawtyanswers" target="_blank"> <img src="/imgs/shawtyanswers.jpg" alt="Swaty's Image" class="image" style="float:right;"></a> -->
* Binary Class -   
* No Class imbalance  

`INPUT:` Image - 3D MRI Scan

<center>
<img src="/imgs/dataset.jpg" alt="drawing" width="50%" >
</center>
<br>
`INPUT SIZE: (Width * Height * Channels (R,G,B))`  
* <span style="color:green">__PATH 1:__</span>  : 25px * 25px * 3 (Normal resolution)
* <span style="color:blue">__PATH 2:__</span>  : 19px * 19px * 3  (Low resolution)

___  
___  
<br>
`ARCHITECTURE:`

`CONVOLUTION LAYERS (CONV)`  

<span style="color:green">__PATH 1:__</span>  




`CONV LAYER 1:` <span style="color:green">21 * 21 * 3</span>  | #Filter: 30 | Size: 5 * 5 * 5
`CONV LAYER 2:` <span style="color:green">17 * 17 * 3</span> | #Filter: 40 | Size: 5 * 5 * 5
`CONV LAYER 3:` <span style="color:green">13 * 13 * 3</span> | #Filter: 40 | Size: 5 * 5 * 5
`CONV LAYER 4:` <span style="color:green">9 * 9 * 3</span>  | #Filter: 50 |  Size: 5 * 5 * 5

<span style="color:blue">__PATH 2:__</span>


`CONV LAYER 1:` <span style="color:blue">15 * 15 * 3</span> | #Filter: 30 | Size: 5 * 5 * 5
`CONV LAYER 2:` <span style="color:blue">11 * 11 * 3</span> | #Filter: 40 | Size: 5 * 5 * 5
`CONV LAYER 3:` <span style="color:blue">7 * 7 * 3</span> | #Filter: 40 | Size: 5 * 5 * 5
`CONV LAYER 4:` <span style="color:blue">3 * 3 * 3</span>  | #Filter: 50 |  Size: 5 * 5 * 5

___  
___  

<br>
`CONVOLUTION OPERATION:`

Goal: To learn features and generates feature maps.

> CONVOLUTION OPERATION: This is the formula for computing featuer maps.

<center>
<img src="/imgs/convlutional_operation.png" alt="drawing" width="70%" >
</center>
<br>

> DIMENSIONS:

> NO. OF PARAMETERS:

___  
___  

<br>

`UPSAMPLING:`

<center>
<img src="/imgs/upsampling.png" alt="drawing" width="40%" >
</center>

___  
___  

<br>

`FULLY CONNECTED LAYER:`

Why?  
IN CNN, we combine all the features learnt together (FILTERS), and try classification.

<span style="color:yellow">__LAYER 1:__</span>  

`LAYER 1:` <span style="color:green">9 * 9 * 3 </span>  | #Filter: 150 | Size: 1 * 1 * 1
`LAYER 2:` <span style="color:green">9 * 9 * 3</span> | #Filter: 150 | Size: 1 * 1 * 1


___  
___  

<br>


`CLASSIFICATION LAYER:`

> Softmax function

___  
___  

<br>


`COST FUNCTION:`

<center>
<img src="/imgs/cost_cross_entrophy.png" alt="drawing" width="70%" >
</center>


___  
___  

<br>


`OPTIMIAZATION: STOCASTIC GRADIENT DESCEND`
<center>
<img src="/imgs/SGD.svg" alt="drawing" width="70%" >
</center>


___  
___  

<br>

`CODE SAMPLE: KERAS | PYTORCH`

<script src="https://gist.github.com/nikhilwani/b920896b03abffd50a458d403f6d492c.js"></script>

___  
___  

<br>

`EVALUATION: DICE SCORE`
<center>
<img src="/imgs/results.jpg" alt="drawing" width="70%" >
</center>
<br>


___  
___  

<br>

`FUTURE WORK: How to improve it?`  
* M-RNNs


<!-- <br> -->

<!-- Title:
*Deep* Learning Lessons from Nvidia Internship
If anyone from Nvidia is reading this, thank you for a wonderful experience.



You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/ -->
