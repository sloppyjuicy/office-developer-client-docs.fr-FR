---
title: Variables de modèle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instances de variables de modèle (représentés par un élément templateVariable) spécifient les données d’une activité de flux d’élément dans un modèle d’activité.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787729"
---
# <a name="template-variables"></a>Variables de modèle

Instances de variables de modèle (représentés par un élément **templateVariable** ) spécifient les données d’une activité de flux d’élément dans un modèle d’activité. 
  
Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md).

Le tableau suivant indique les types de variables de modèle pris en charge, que chacun étant représenté par la valeur d’énumération XML correspondante.
  
|**Type de variable de modèle**|**Description**|
|:-----|:-----|
|**entityVariable** <br/> |Une personne, un groupe ou une chose.  <br/> |
|**linkVariable** <br/> |Un lien.  <br/> |
|**listVariable** <br/> |Un groupe d’objets.  <br/> |
|**pictureVariable** <br/> |Image.  <br/> |
|**publisherVariable** <br/> |Élément de flux de l’éditeur de l’activité.  <br/> |
|**textVariable** <br/> |Un bloc de texte.  <br/> |
   
Éléments pour spécifier les données relatives à cette variable est requis pour chaque type de variable de modèle. Variables de modèle sont spécifiés comme suit :
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variable de modèle de liste

Vous pouvez spécifier des variables de modèle qui sont contenues dans une liste (délimitée par les éléments **listVariable** et **listItems** ) comme suit : 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Une variable de modèle de type **listVariable** est un conteneur pour les objets. Il peut contenir les éléments délimité par des virgules (du type **linkVariable** ou **textVariable** ) ou des images (du type **pictureVariable** ). Listes peuvent contenir jusqu'à cinq lier des éléments, cinq éléments de texte ou cinq images. 
  
L’Outlook Social Connector (OSC) localise lien ou du texte des éléments de liste en fonction des paramètres régionaux du système de Windows.
  
Pour analyser et afficher des images dans un élément de flux d’activités correctement, vous devez inclure des images dans une liste. Toutes les images sont redimensionnés pour être 52 pixels de haut. La largeur de l’image n’est pas redimensionnée.
  
## <a name="template-variable-elements"></a>Éléments de variables de modèle

Cette section décrit les éléments requis et facultatifs pris en charge pour chaque type de variable de modèle.
  
### <a name="entityvariable"></a>entityVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Le nom de la variable. Obligatoire.  <br/> |
|**id** <br/> |ID unique de l’utilisateur. Obligatoire.  <br/> |
|**nameHint** <br/> |Le nom à afficher dans l’élément de flux. Facultatif.  <br/> |
|**profileUrl** <br/> |L’URL du profil de la personne qui sera utilisé comme le lien hypertexte pour le nom de la personne dans l’élément de flux, si le nom de personne n’est présent. Facultatif.  <br/> |
|**emailAddress** <br/> |L’adresse de messagerie qui sert à mettre à jour les informations de contact de cette personne dans Outlook. Facultatif.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Le nom de la variable. Obligatoire.  <br/> |
|**valeur** <br/> |L’URL pour ce lien. Obligatoire.  <br/> |
|**text** <br/> |Le texte à afficher au lieu de l’URL du lien. Facultatif.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Le nom de la variable. Obligatoire.  <br/> |
|**listItems** <br/> |Conteneur pour les éléments dans la liste. Obligatoire.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Le nom de la variable. Obligatoire.  <br/> |
|**valeur** <br/> |L’URL de l’image. Obligatoire.  <br/> |
|**altText** <br/> |Le texte de remplacement à afficher pour l’accessibilité et lorsque l’utilisateur déplace le pointeur de la souris sur l’image. Facultatif.  <br/> |
|**href** <br/> |Le lien hypertexte à utiliser lorsque l’utilisateur clique sur l’image, si la cible souhaitée n’est pas l’URL de l’image spécifiée par l’élément de **valeur** . Facultatif.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Le nom de la variable. Obligatoire.  <br/> |
|**id** <br/> |ID unique de l’utilisateur. Obligatoire.  <br/> |
|**nameHint** <br/> |Le nom à afficher dans l’élément de flux. Facultatif.  <br/> |
|**profileUrl** <br/> |L’URL du profil de la personne qui sera utilisé comme le lien hypertexte pour le nom de la personne dans l’élément de flux, si le nom de personne n’est présent. Facultatif.  <br/> |
|**emailAddress** <br/> |L’adresse de messagerie qui sert à mettre à jour les informations de contact de cette personne dans Outlook. Facultatif.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Le nom de la variable. Obligatoire.  <br/> |
|**valeur** <br/> |Le texte à afficher. Facultatif.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du code XML pour une activité de flux d’élément](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails, élément](activitydetails-element.md)  
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)  
- [Conseils pour l’affichage correctement les activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Fournisseur Outlook Social Connector schéma XML](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

