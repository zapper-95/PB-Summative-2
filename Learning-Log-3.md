## Entry 3:
From my last entry, I wanted to be able to increase the confidence on the model in identifying Phobos, as well as identifiying some more satellites. I started by finding some more photos of Phobos and adding it to the training folder. From my research of neural networks, I wanted to make sure not to include too many similar taken photos in the training folder. For example, if I included only photos of Phobos where all of it can be seen, then the model might associate that as a feature of being Phobos, and not recognise a close up picture as being it. I believe this may have led to the lower confidence score that I saw before, so I reorganised which pictures were in the training and testing folder so that there were a mixture of close and far ones. Whether due to having more training images, or a wider mixture of pictures more generally representing it, the confidence of the same image as in the last entry improved from 0.52 to 0.64.

![Phobos2](Learning-Log/phobos2.png)

Unfortunately, I noticed that the confidence that it was an asteroid slightly increased from last time from 0.3 to 0.33. However, I believe because the increase is a lot smaller than that of the correct label, that the changes I made were overall good for the model.

To expand the range of satellites the model could identify, I choose the moons Ganymede of Jupiter and Tethys of Saturn. I found it difficult, especially for Ganymede, to get enough good images to train it on. A lot of the images were really close up, or more scientific images with annotation on. As before, I tried to divide the images so that there was a good range of close up and further away ones.    

The images below show me testing out the model with two examples. For both of these it confidently managed to guess the correct label.
![Ganymede](Learning-Log/ganymede.png)
![Tethys](Learning-Log/tethys.png)


The overall accuracy of the model slightly improved, with an increase from 84% to 85.7%. This is obviously good, however, I think if I introduced many more satellites, this would drop, as it might start confusing them with one another.

Finally, I made a commit with these changes to Github and I am now waiting to see what changes I might need to make if the pull request is rejected. In the meantime I will begin training the model on recognising comets, which is another flagged issue. 
