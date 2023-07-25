# 2D to 3D Models
## 1. PIFuHD

- [GitHub Repo](https://github.com/facebookresearch/pifuhd)
- [Colab](https://colab.research.google.com/drive/11z58bl3meSzo6kFqkahMa35G5jmh2Wgt?usp=sharing)

The testing images are all background-removed by [Adobe Express](https://express.adobe.com/tools/remove-background).

### Results

1. French Lady v2, 2k, AI generated

https://github.com/randaldong/2Dto3D/assets/55754917/48a24b79-7e1f-4dc4-9416-471f590a9ac3

2. French Lady v1, 2k, AI generated

https://github.com/randaldong/2Dto3D/assets/55754917/2068ffa0-448b-46f0-9ede-47f345b6dd64

3. Old men, 1k, AI generated, from [CIVITAI](https://civitai.com/images/1318029?modelVersionId=105035&prioritizedUserIds=81744&period=AllTime&sort=Most+Reactions&limit=20)

https://github.com/randaldong/2Dto3D/assets/55754917/21d0fb83-89bf-4155-8ab6-dafb2fe38950

4. Eponine in Les Misérables, still, from [Internet](https://movie.douban.com/photos/photo/1855235220/#title-anchor)

https://github.com/randaldong/2Dto3D/assets/55754917/786a55e5-54c5-4ba6-9815-8cd8874fdf1f

The first three results are all generated from AI-generated images, while the last one is a real photograph. It seems that PIFuHD has a bad performance on AI-generated images.

## 2. ZoeDepth

- [HuggingFace](https://huggingface.co/spaces/shariqfarooq/ZoeDepth)
- [GitHub Repo](https://github.com/isl-org/ZoeDepth)
- [Colab](https://colab.research.google.com/drive/11z58bl3meSzo6kFqkahMa35G5jmh2Wgt?usp=sharing)

The testing images are all background-removed by [Adobe Express](https://express.adobe.com/tools/remove-background).

### Results

The output is viewed using a [online glTF viewer](https://gltf-viewer.donmccurdy.com/) that allows custom lighting.

1. French Lady v2, 2k, AI generated

[Watch the video result on YouTube](https://youtu.be/J0DKF72572M)

![IMAGE ALT TEXT HERE](https://i.imgur.com/9m8Eegy.jpg)

2. French Lady v1, 2k, AI generated

[Watch the video result on YouTube](https://youtu.be/2Q3JrWSQsC8)

![IMAGE ALT TEXT HERE](https://i.imgur.com/vXukfXb.jpg)

3. Old men, 1k, AI generated, from [CIVITAI](https://civitai.com/images/1318029?modelVersionId=105035&prioritizedUserIds=81744&period=AllTime&sort=Most+Reactions&limit=20)

[Watch the video result on YouTube](https://youtu.be/HdOqY-pHu7s)

![IMAGE ALT TEXT HERE](https://i.imgur.com/RYmZOIi.jpg)

4. Eponine in Les Misérables, still, from [Internet](https://movie.douban.com/photos/photo/1855235220/#title-anchor)

[Watch the video result on YouTube](https://youtu.be/7iX_8lQ2An8)

![IMAGE ALT TEXT HERE](https://i.imgur.com/YlWqSIb.jpg)

From the above results, the following conclusions can be drawn:
- ZoeDepth works much better on converting 2D images to 3D models than PIFuHD.
- ZoeDepth only cares about the details in the image, no matter if it's a real photograph or an AI-generated image (This differs a lot from PIFuHD which has a very bad performance on AI-generated images).
- The resolution of ZeoDepth is satisfying and depends on lighting and quality of the original image.
- Though the generated model in the glTF viewer looks a little bit "pale", we can always change the lighting later in game engines
- The 3D model generated by ZoeDepth looks the best when viewed from the same angle as the image. In other words, when viewed from a different perspective, the model is still not so realistic.
