---
title: "Cosine Similarity and Cosine Distance"
date: 2022-07-03T01:24:21+05:30
author: 'Rigved'
draft: False
---

In this section we're going to talk about two very simple concepts of cosine similarity and cosine distance

### Cosine similarity

Cosine similarity is just a basic mathematical concept that we have used in higher algebra. It is simply the cosine of the angle between the two vectors. It can be calculated by finding the dot product between the vectors and dividing it by the product of the magnitude of the vectors.    
Formula:   
S.Q / (||S||  ||Q||)  
Obviously the value is going to lie between 0 and 1    
If the vectors are perpendicular to each other then final answer is zero. This is highly useful in recommendation systems.  
For Example: If we plot the the genres of movies on different axis where suppose action movies are on x axis and romantic movies are on y axis. The cosine similarity between them is 0 and thus it will help the algorithm in better recommendation of the movies to the user.

### Cosine distance

Cosine distance is nothing but 1 - cosine_similarity. That's it. It is that simple calculation wise. 


### Sharpened cosine similarity

In this, we find the cosine of the angle between the vectors and then raising the magnitude of the result to a power p while maintaining the sign.  
 
scs(s,k)=sign(s⋅k)(s⋅k(∥s∥+q)(∥k∥+q))^p  

A great advantage of this method has been in increased parameter efficency. The SCS produces very interpretable feature maps.  
A thing to keep in mind while using this method is to use AbsMAxPooling instead of simple MaxPooling since we are now maintaining the sign, we want the element with the highest magnitude (which can also be negative)
