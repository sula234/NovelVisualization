# NovelVisualization
**Автоматическая иллюстрация художественных произведений**

<a target="_blank" href="https://colab.research.google.com/github/sula234/NovelVisualization/blob/main/NovelVisualization.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

In this work, the capabilities of the **Stable Diffusion** and **Meaning Cloud** deep learning models were demonstrated using the example of the task of automatically generating images based on famous novels. As the results showed, the model for generating images requires a very clear description and even so, does not always produce meaningful results. Moreover, the problem is exacerbated by not clear text reduction and other limitations of the models used in this paper. However, decent results were also obtained, which will be demonstrated below.

The Stable Diffusion model was used to generate images based on text descriptions. Meaning Cloud analyzed the text and shortened it, conveying the main meaning. To simplify the work with the text, it was decided to analyze 1-2 paragraphs. This approach is very simple, and the implementation does not require much time. However, the quality of the resulting images may suffer. The text should be as accurate and detailed as possible, otherwise, we get distorted images. For illustration, the first few chapters of the famous fairy tale Puss in Boots were chosen. Below is the abbreviated text and the resulting image. As you can see, in order not to repeat proper names, the author uses pronouns. However, during processing, the model does not understand who it is about and starts to confuse the characters. Therefore, instead of a jubilant Puss in Boots, we get a rat.

![image4](https://user-images.githubusercontent.com/91324982/222164456-161f3a9c-58dd-4182-8756-988536ddd776.jpg)
*"Hurray!" he cried, as he reached the front door, and he took a hop, skip, and jump across the piazza, holding his tail gracefully in his left paw. "Hurray!"Down the steps he skipped, two at a time, down the walk to the gate, his heels clattering on the stone pavement, rat-a-tat-tat, like a cavalryman. The road was dusty, but he went along gaily, the sun shining on the bright red tops of his boots, making him very proud indeed.'*

Many other paragraphs without context are rendered meaningless to Stable Diffusion, or generally too complex to portray properly. However, some are still successful. In the same story about Puss in Boots, there is a scene where he finds a pig stuck in a fence.

![image2](https://user-images.githubusercontent.com/91324982/222165057-208ad844-e0ff-46d1-89b3-1abe9fec525f.jpg)
*He hadn't gone very far when he heard a funny little squeak, and,
looking to the side of the road from which the sound came, he saw a
small pig stuck between two boards in the fence.*

It is also worth noting that this approach illustrates paragraphs with descriptions of heroes very well. The following are illustrations for The Picture of Dorian Gray. However, the good results may be due to the fact that films were made using the novel, and many of the movie characters are very similar to the resulting images.
![image3](https://user-images.githubusercontent.com/91324982/222165646-321f66fa-85b8-4f64-aef1-572a1c1f4d17.jpg)
*“Harry,” said Basil Hallward, looking him straight in the face, “every
portrait that is painted with feeling is a portrait of the artist, not
of the sitter. The sitter is merely the accident, the occasion. It is
not he who is revealed by the painter; it is rather the painter who, on
the coloured canvas, reveals himself. The reason I will not exhibit
this picture is that I am afraid that I have shown in it the secret of
my own soul.”*

![image1](https://user-images.githubusercontent.com/91324982/222165934-f9b0ace6-3ab6-49d6-a027-a61bf8960ffe.jpg)
*Lord Henry elevated his eyebrows and looked at him in amazement through
the thin blue wreaths of smoke that curled up in such fanciful whorls
from his heavy, opium-tainted cigarette. “Not send it anywhere? My dear
fellow, why? Have you any reason? What odd chaps you painters are! You
do anything in the world to gain a reputation. As soon as you have one,
you seem to want to throw it away…*

![image5](https://user-images.githubusercontent.com/91324982/222166142-ee9f7b03-2754-42f6-a3cb-7f1af8949613.jpg)
*“He is all my art to me now,” said the painter gravely. “I sometimes
think, Harry, that there are only two eras of any importance in the
world’s history. The first is the appearance of a new medium for art,
and the second is the appearance of a new personality for art also.
What the invention of oil-painting was to the Venetians, the face of
Antinous was to late Greek sculpture, and the face of Dorian Gray will
some day be to me. It is not merely that I paint from him, draw from
him, sketch from him. Of course, I have done all that. But he is much
more to me than a model or a …*

In conclusion, I would like to note that for 10 unsuccessful images, there is one worthy one. To improve this result, more advanced algorithms for paragraph reduction and models for generation should be applied. For example, you can analyze the previous paragraphs and find who is being referred to in this paragraph if the hero is indicated by a pronoun. However, if we take into account that there are usually not so many images in books (about 10 per book), then the results can be considered satisfactory.

*The code for this work is provided in the corresponding Google Colab notebook.*




