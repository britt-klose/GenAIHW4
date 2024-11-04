# GenAIHW4

# Discussion Points

## Trade-off between generating high-quality images and maintaining diversity in the output. 
**I.E. Are the generated images too similar, or does the model capture a wide range of bedroom styles?**

* Based on the tests I’ve run and the ones we have seen in class generating higher quality images typically means a lower display of diversity in the output. My GAN specifically faces the issue of generating images that were all essentially the same. The quality wasn’t bad for my first GAN but I was expecting higher to make up for the lack of diversity. Specifically they were all very dark and required me to increase my brightness to get more clarity. Though this could have been somewhat attributed to my color palette.

## Enhancements to the model architecture/training process: 
**EX. Would experimenting with different hyperparameters or batch sizes yield better results?**
* Changing the **batch size** can affect the GAN performance. As we learned in class, increasing the batch size offers faster training, but doesn’t necessarily lead to better performance. In fact making the batch size too large can cause the GAN to produce outputs that are very similar and cause the discriminator to overfit. Decreasing the batch size on the other hand can offer more diversity and higher quality in the generated images. The batch size here was 256. I tested this by decreasing the batch size to 100. This unfortunately did not have any noticeable effect in my results though the training time did increase.
  
* Increasing the **number of epochs** can also help enhance performance though it can significantly add to training time. Additionally, too much training can cause the generated images to be less diverse and too similar to training samples. A small adjustment to 100 epochs instead of 50 could reasonably increase performance.
  
* Lastly, **changing the sample size** can help with performance. The original sample size included over 300,000 images. My GAN in comparison was trained only on about 1,000 photos to conserve memory and make the training process more efficient. If I were to add another 1,000 photos to my sample it could offer more diversity to my GAN model.

## What are the practical applications for this type of generative model?
* There are many applications for gan that this assignment provides good practice for. In particular this type of generative model is good for image to image translation. My model, while not as efficient as desired, was made to be able to translate colors of photos and placement of objects to offer various designs for bedrooms. Which would serve as a great tool for designing any type of room or interiors. Additionally, this model used bedroom images but it could easily be applied to designing clothing apparel by using clothing images to see new desings with different colors and combinations. 

## Consider how you might quantitatively evaluate the quality of the generated images.
**Hint: Inception Score (IS) or Inception Distance (ID) can provide measures of image quality and diversity.**
* **The Inception Score (IS**) is one way to help quantitatively evaluate the quality of generated images. IS offers a measure for how confidently a pre-trained image classifier can classify generated images into distinct categories while also maintaining multiple classes across the set. The higher the IS score the better the image quality and presence of diversity is. Overall an IS score is typically utilized to offer a more quantitative feedback versus just human feedback on how well the new images appear.
  
* **The Inception Distance(ID**) also offers helpful quantitative feedback regarding the quality of generated images by providing a comparison between generated images and real images. Specifically, it compares the distribution of features between them and offers a quantitative grade for how similar the images are. In this case a user wants the ID measure to be low. This means the generated images display significantly high quality and resemblance to the real image distribution, i.e. the images appear very real when they’re fake.  
