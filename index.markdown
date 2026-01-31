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


# Attendance

# Visio conference



<details style="background-color: #f0f8ff; border: 1px solid #ccc; border-radius: 8px; padding: 15px; margin-bottom: 15px;">
  <summary style="cursor: pointer; font-weight: bold; font-size: 1.1em; background-color: #007bff; color: white; padding: 8px 12px; border-radius: 5px; display: inline-block;">
    Abstract
  </summary>

  <p style="margin-top: 10px; line-height: 1.5; color: #333;">
This thesis focuses on indexing and retrieval in 3D point clouds for large-scale place recognition, and more precisely on its acceleration. The objective is to search for point clouds similar to a query cloud in a database of georeferenced point clouds by establishing a representation of the point cloud and then searching for it in the database to obtain a list of nearest neighbors ranked by similarity according to distance metrics. 

State-of-the-art methods in place recognition from point clouds primarily focus on building representations of the cloud rather than on the efficient search for similar candidates. This second step typically relies on exhaustive search or better k-d trees, making it computationally expensive when the volume of the point cloud reference database increases or is inefficient in high dimensions. This is, however, a typical situation in current geographic information applications, such as large-scale place recognition or reference updates. In contrast, the literature on the subject, mainly in robotics, primarily focuses on loop closure scenarios, often limited to the scale of a street or neighborhood. To address this problem, we have chosen to draw inspiration from the state of the art in information retrieval. This thesis makes three contributions to the problem of large-scale place recognition, relying exclusively on the geometric information contained in point clouds.

Our first contribution, called DSI-3D, is based on the Differentiable Search Index (DSI) approach, which can generate identifiers for relevant documents in response to a textual query. To associate such indices with 3D data, we draw inspiration from Vision Transformers, such as GIT, which were originally designed for image captioning. By replacing its image encoder with a 3D encoder, our method learns to generate indices from point clouds, enabling similarity searches of point clouds in constant inference time. Several encoding strategies, some specialized for geolocation, have been studied and evaluated using the standard datasets from the state of the art in robotics (KITTI).

Our second contribution is the exploitation of LiDAR-based territorial mapping data, LiDAR HD from the IGN, for place recognition tasks. This dataset, present throughout the entire French territory, has acquisition characteristics that differ significantly from those of mobile mapping. The use of DSI-3D on this dataset thus required fine-tuning of the 3D encoder and adaptation strategies. To assess the generalization capability of DSI-3D, two areas of Paris were selected to form the new evaluation dataset.

Our final contribution explores two improvements for retrieval in 3D point clouds, aimed at scaling to larger areas and at improving the quality of the retrieval. First, we investigated a retrieval strategy based on Mixtures of Experts (MoE), which divides the model into distinct sub-models (experts), each specialized in a subset of the database. Second, we studied the application of a re-ranking mechanism to improve point cloud place recognition performance by re-ordering the list of candidates based on their local feature similarity.

This work is intended to open perspectives on improving large-scale retrieval in 3D point clouds for place recognition, particularly with regard to the use of generative search, while stimulating future research on the integration of multimodal methods for place recognition.
  </p>
</details>


<details style="background-color: #f0f8ff; border: 1px solid #ccc; border-radius: 8px; padding: 15px; margin-bottom: 15px;">
  <summary style="cursor: pointer; font-weight: bold; font-size: 1.1em; background-color: #007bff; color: white; padding: 8px 12px; border-radius: 5px; display: inline-block;">
    Résumé
  </summary>

  <p style="margin-top: 10px; line-height: 1.5; color: #333;">
Cette thèse porte sur l'indexation et l'accélération de la recherche dans les nuages de points 3D, pour la reconnaissance de lieux à grande échelle. L'objectif est de rechercher des nuages similaires à un nuage requête dans une base de données de nuages géoréférencés, en établissant une représentation du nuage, puis en la recherchant dans la base pour obtenir une liste de candidats triés par ordre de similarité.

Les méthodes de l'état de l'art en reconnaissance de lieux à partir de nuages de points se concentrent principalement sur la construction de la représentation des nuages, plutôt que sur une recherche efficace de candidats similaires. Cette seconde étape repose généralement sur une recherche exhaustive, au mieux avec un arbre k-d, ce qui la rend coûteuse en temps de calcul lorsque le volume du référentiel de nuages de points augmente, ou moins intéressante pour des vecteurs de grande dimension. C'est pourtant une situation typique dans les applications actuelles de l'information géographique, telles que la reconnaissance de lieux à grande échelle ou la mise à jour des référentiels. À l'inverse, la littérature sur le sujet en robotique se concentre majoritairement sur des scénarios de fermeture de boucle, souvent limités à l'échelle d'une rue ou d'un quartier. Pour répondre à ce problème, nous avons choisi de nous inspirer des méthodes de recherche d'information de l'état de l'art. Cette thèse apporte trois contributions à la problématique de la reconnaissance de lieux à grande échelle, en s'appuyant exclusivement sur les informations géométriques contenues dans les nuages de points.

Notre première contribution, nommée DSI-3D, repose sur l'approche du Differentiable Search Index (DSI), capable de générer l'identifiant des documents pertinents en réponse à une requête textuelle. Pour associer ce type d'indices aux données 3D, nous nous inspirons des Vision Transformers tels que GIT, conçus initialement pour la génération automatique de descriptions d'images. En remplaçant l'encodeur d'image par un encodeur 3D, notre méthode apprend à générer des indices à partir de nuages de points, ce qui permet une recherche de nuages de points similaires en temps d'inférence constant. Plusieurs stratégies d'encodage, spécialisées pour la géolocalisation, ont été étudiées et évaluées sur un jeu de données de l'état de l'art en robotique (KITTI).

Notre seconde contribution consiste en l'adaptation des données de cartographie territoriale LiDAR HD de l'IGN, présentes sur tout le territoire français, à des tâches de reconnaissance de lieux. Ce jeu de données présente des caractéristiques d'acquisition sensiblement différentes de celles de la cartographie mobile, mais il offre la possibilité d'être étendu à l'échelle nationale. Cette évaluation a nécessité un nouvel entraînement de l'encodeur 3D, impliquant un découpage du jeu de données en ensembles d'apprentissage et d'évaluation.
Afin d'évaluer la capacité de généralisation des descripteurs appris, deux zones de Paris ont été sélectionnées pour valider cet entraînement. 

Notre dernière contribution explore deux améliorations de DSI-3D, conçues pour s'adapter aux grands jeux de données. Premièrement, nous étudions une stratégie de recherche basée sur les mélanges d'experts (Mixtures of Experts, MoE). Leur principe consiste à scinder un modèle d'apprentissage en plusieurs sous-modèles indépendants, appelés experts, chacun étant spécialisé dans un sous-ensemble spécifique de nuages de points. Deuxièmement, dans le cadre d'un stage de Master, nous étudions l'application d'un mécanisme de reclassement pour améliorer les performances de la reconnaissance de lieux dans les nuages de points, en réorganisant la liste des candidats selon la similarité de leurs caractéristiques locales.

Ce travail vise à ouvrir des perspectives sur l'amélioration de la reconnaissance de lieux à grande échelle à partir de nuages de points 3D, en particulier en ce qui concerne l'utilisation de la recherche générative, tout en stimulant les recherches futures sur l'intégration de méthodes multimodales pour la reconnaissance de lieux.
  </p>
</details>





# References
{% include text-expand.html %}











