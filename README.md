# NovelVisualization
**Автоматическая иллюстрация художественных произведений**

В данной работе были продемонстрированы возможности моделей глубокого обучения **Stable Diffusion**  и **Meaning Cloud** на примере задачи автоматической генерации изображений на базе знаменитых художественных произведений. Как показали результаты, модель для генерации изображений требует очень четкого описания и даже так не всегда выдает осмысленные результаты. Более того, проблема ухудшается неуклюжим сокращением текста и другими ограничениями моделей, использованных в данной работе. Однако были получены и достойные результаты, которые будут продемонстрированы ниже.

Модель Stable Diffusion была использована для генерации изображений на базе текстовых описаний. Meaning Cloud анализировала текст и сокращала его, передавая основной смысл. Чтобы упростить работу с текстом, было решено анализировать по 1-2 абзаца. Данный подход очень простой, и реализация не требует много времени. Однако может страдать качество полученных изображений. Текст должен быть максимально точным и подробным, иначе мы получаем искаженные изображения. Для иллюстрации были выбраны первые несколько глав знаменитой сказки Кот в сапогах. Ниже приведен сокращенный текст и полученное изображение. Как видим, чтобы не повторять имена собственные, автор использует местоимения. Однако при обработке модель не понимает, о ком идет речь, и начинает использовать то, что есть. Поэтому вместо ликующего Кота в сапогах мы получаем крысу.

![image4](https://user-images.githubusercontent.com/91324982/222164456-161f3a9c-58dd-4182-8756-988536ddd776.jpg)
*"Hurray!" he cried, as he reached the front door, and he took a hop,skip, and jump across the piazza, holding his tail gracefully in his left paw. "Hurray!"Down the steps he skipped, two at a time, down the walk to the gate, his heels clattering on the stone pavement, rat-a-tat-tat, like a cavalryman. The road was dusty, but he went along gaily, the sun shining on the bright-red tops of his boots, making him very proud indeed.'*

Многие другие абзацы без контекста получаются бессмысленными для Stable Diffusion или в целом слишком сложными, чтобы дать правильное изображение. Однако некоторые все таки получаются удачными. В той же самой cказке о  Коте в сапогах есть сцена, где он находит застрявшую свинку в заборе.

![image2](https://user-images.githubusercontent.com/91324982/222165057-208ad844-e0ff-46d1-89b3-1abe9fec525f.jpg)
*He hadn't gone very far when he heard a funny little squeak, and,
looking to the side of the road from which the sound came, he saw a
small pig stuck between two boards in the fence.*

Также стоит отметить, что данный подход очень хорошо иллюстрирует абзацы с описанием героев. Далее приведены иллюстрации для романа Портрет Дориан Грей. Однако хорошие результаты могут быть связаны с тем, что по данному роману снимали фильм, и многие герои очень похожи на полученные изображения.
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

В заключении хотелось бы отметить, что на 10 неудачных изображений приходится по одной достойной. Чтобы улучшить данный результат, следует применять более улучшенные алгоритмы для сокращения абазцев и модели для генерации. Например, можно анализировать предыдущие абзацы и находить, о ком говорится в данном абзаце, если герой указан местоимением. Однако если учитывать, что в книгах не так уж и много обычно изображений(около 10 на книгу), то результаты могут считаться удовлетворительными.

*Код для данной работы представлен в соответствующем Google Colab блокноте.* 




