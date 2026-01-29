---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: page
header_img : /assets/header.png
---


![]({{page.header_img | relative_url}})

<br/>

[Chahine-Nicolas Zede](https://www.umr-lastig.fr/Chahine-Nicolas-Zede/),
[Laurent Caraffa](https://www.umr-lastig.fr/laurent-caraffa/),
[Valérie Gouet-Brunet](https://www.umr-lastig.fr/vgouet/),
{: style="color:gray; font-size: 120%; text-align: center;"}

# Pdf
[hal](https://hal.science/hal-05345963/document)

# Abstract

<details>
  <summary>Click to read abstract</summary>
  
  This is the full abstract paragraph. It can be multiple sentences,
  include **bold**, *italic*, or links like [GitHub](https://github.com).  
  It will only be visible when the user clicks the summary above.
</details>


This thesis focuses on indexing and retrieval in 3D point clouds for large-scale place recognition, and more precisely on its acceleration. The objective is to search for point clouds similar to a query cloud in a database of georeferenced point clouds by establishing a representation of the point cloud and then searching for it in the database to obtain a list of nearest neighbors ranked by similarity according to distance metrics. 

State-of-the-art methods in place recognition from point clouds primarily focus on building representations of the cloud rather than on the efficient search for similar candidates. This second step typically relies on exhaustive search or better $k$-d trees, making it computationally expensive when the volume of the point cloud reference database increases or is inefficient in high dimensions. This is, however, a typical situation in current geographic information applications, such as large-scale place recognition or reference updates. In contrast, the literature on the subject, mainly in robotics, primarily focuses on loop closure scenarios, often limited to the scale of a street or neighborhood. To address this problem, we have chosen to draw inspiration from the state of the art in information retrieval. This thesis makes three contributions to the problem of large-scale place recognition, relying exclusively on the geometric information contained in point clouds.

Our first contribution, called DSI-3D, is based on the Differentiable Search Index (DSI) approach, which can generate identifiers for relevant documents in response to a textual query. To associate such indices with 3D data, we draw inspiration from Vision Transformers, such as GIT, which were originally designed for image captioning. By replacing its image encoder with a 3D encoder, our method learns to generate indices from point clouds, enabling similarity searches of point clouds in constant inference time. Several encoding strategies, some specialized for geolocation, have been studied and evaluated using the standard datasets from the state of the art in robotics (KITTI).

Our second contribution is the exploitation of LiDAR-based territorial mapping data, LiDAR HD from the IGN, for place recognition tasks. This dataset, present throughout the entire French territory, has acquisition characteristics that differ significantly from those of mobile mapping. The use of DSI-3D on this dataset thus required fine-tuning of the 3D encoder and adaptation strategies. To assess the generalization capability of DSI-3D, two areas of Paris were selected to form the new evaluation dataset.

Our final contribution explores two improvements for retrieval in 3D point clouds, aimed at scaling to larger areas and at improving the quality of the retrieval. First, we investigated a retrieval strategy based on Mixtures of Experts (MoE), which divides the model into distinct sub-models (experts), each specialized in a subset of the database. Second, we studied the application of a re-ranking mechanism to improve point cloud place recognition performance by re-ordering the list of candidates based on their local feature similarity.

This work is intended to open perspectives on improving large-scale retrieval in 3D point clouds for place recognition, particularly with regard to the use of generative search, while stimulating future research on the integration of multimodal methods for place recognition.



# Code
[Github](https://github.com/Chahine-Nicolas/DSI-3D)

# News
 - 2025-28-10 : Page online

# References

{% highlight bibtex %}
@inproceedings{caraffa:hal-03380593,
  TITLE = {DSI-3D: Differentiable Search Index for Point Cloud Retrieval},
  AUTHOR = {ZEDE, Chahine-Nicolas and CARAFFA, Laurent and GOUET-BRUNET, Valérie},
  URL = coming soon,
  BOOKTITLE = {2025 International Conference on Content-Based Multimedia Indexing (CBMI)},
  ADDRESS = {Dublin, Ireland},
  YEAR = {2025},
  MONTH = Oct,
  PDF = coming soon,
  HAL_ID = coming soon,
  HAL_VERSION = {v1},
}
{% endhighlight %}
{% include text-expand.html %}




