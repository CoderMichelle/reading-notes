# Reading Notes 14a

With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property. The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

Transform Syntax  - This works in both 2D and 3D

div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
 Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth.  2D Rotate --The transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically.  HTML : 

<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
CSS :  

.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
2D Scale - Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger. HTML :

<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
CSS :

.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}
8 simple CSS3 transitions :
Fade in
Change Color
Grow & Shrink
Rotate Elements
Square to Circle
3D Shadow
Swing
Inset Border
CSS
Transitions
Shorthand Transitions
Animations
Customizing Animations
 (Links to an external site.)Shorthand Animations

 ## Reading Notes 14b 


What Google Learned From Its Quest to Build the Perfect Team 

New York Times Magazine By Charles Duhigg

Feb. 25, 2016

Many of today’s most valuable firms have come to realize that analyzing and improving individual workers ­— a practice known as ‘‘employee performance optimization’’ — isn’t enough. In 2012, Google embarked on an initiative — code-named Project Aristotle, to study hundreds of Google’s teams and figure out why some stumbled while others soared, with the focus on building the perfect team. In the last decade, the tech giant has spent untold millions of dollars measuring nearly every aspect of its employees’ lives to see how workers can transform productivity.

After looking at over a hundred groups for more than a year, Project Aristotle researchers concluded that understanding and influencing group norms were the keys to improving Google’s teams. What they discovered was that psychological safety was the key component. The behaviors that create psychological safety — conversational turn-taking and empathy — are part of the same unwritten rules we often turn to, as individuals, when we need to establish a bond. And those human bonds matter as much at work as anywhere else. In fact, they sometimes matter more.

What Project Aristotle has taught people within Google is that no one wants to put on a ‘‘work face’’ when they get to the office. No one wants to leave part of their personality and inner life at home. But to be fully present at work, to feel ‘‘psychologically safe,’’ we must know that we can be free enough, sometimes, to share the things that scare us without fear of recriminations. We must be able to talk about what is messy or sad, to have hard conversations with colleagues who are driving us crazy. We can’t be focused just on efficiency. Rather, when we start the morning by collaborating with a team of engineers and then send emails to our marketing colleagues and then jump on a conference call, we want to know that those people really hear us. We want to know that work is more than just labor.
