---
title: Variables de modèle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Les instances de variables de modèle (représentées par un élément templateVariable) spécifient les données d’un élément de flux d’activités dans un modèle d’activité.
ms.openlocfilehash: 37009fe62e0b766ea0c2462f8e9d32a63a96f975
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779629"
---
# <a name="template-variables"></a>Variables de modèle

Les instances de variables de modèle (représentées par un élément **templateVariable** ) spécifient les données d’un élément de flux d’activités dans un modèle d’activité. 
  
Pour obtenir un exemple de données XML de flux d’activités, voir [l’exemple XML des flux d’activités](activity-feed-xml-example.md).

Le tableau suivant indique les types de variables de modèles pris en charge, chacune représentée par la valeur d’éumération XML correspondante.
  
|**Type de variable de modèle**|**Description**|
|:-----|:-----|
|**entityVariable** <br/> |Une personne, un groupe ou une chose. |
|**linkVariable** <br/> |Lien. |
|**listVariable** <br/> |Groupe d’objets. |
|**pictureVariable** <br/> |Image. |
|**publisherVariable** <br/> |Éditeur de l’élément de flux d’activités. |
|**textVariable** <br/> |Bloc de texte. |
   
Chaque type de variable de modèle a des éléments requis pour spécifier les données relatives à cette variable. Les variables de modèle sont spécifiées comme suit :
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Variable de modèle de liste

Vous pouvez spécifier des variables de modèle contenues dans une liste (délimitées par les éléments **listVariable** et **listItems** ) comme suit : 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Une variable de modèle du type **listVariable** est un conteneur d’objets. Il peut contenir des éléments délimités par des virgules (de type **linkVariable** ou **textVariable** ) ou des images (du type **pictureVariable** ). Les listes peuvent contenir jusqu’à cinq éléments de lien, cinq éléments de texte ou cinq images. 
  
Le Outlook Social Connector (OSC) localise les éléments de lien ou de liste de texte en fonction des Windows du système.
  
Pour pouvoir correctement l’afficher et l’afficher dans un élément de flux d’activités, vous devez inclure des images dans une liste. Toutes les images ont une hauteur de 52 pixels. La largeur de l’image n’est pas resa re resserrisée.
  
## <a name="template-variable-elements"></a>Éléments de variable de modèle

Cette section couvre les éléments obligatoires et facultatifs pris en charge pour chaque type de variable de modèle.
  
### <a name="entityvariable"></a>entityVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Nom de la variable. Obligatoire. |
|**id** <br/> |ID unique de l’utilisateur. Obligatoire. |
|**nameHint** <br/> |Nom à afficher dans l’élément de flux. Facultatif. |
|**profileUrl** <br/> |URL du profil de la personne qui sera utilisée comme lien hypertexte pour le nom de la personne dans l’élément de flux, si le nom de la personne est présent. Facultatif. |
|**emailAddress** <br/> |Adresse de messagerie utilisée pour mettre à jour les informations de contact de cette personne dans Outlook. Facultatif. |
   
### <a name="linkvariable"></a>linkVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Nom de la variable. Obligatoire. |
|**value** <br/> |URL de ce lien. Obligatoire. |
|**text** <br/> |Texte du lien à afficher au lieu de l’URL proprement dite. Facultatif. |
   
### <a name="listvariable"></a>listVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Nom de la variable. Obligatoire. |
|**listItems** <br/> |Conteneur pour les éléments de la liste. Obligatoire. |
   
### <a name="picturevariable"></a>pictureVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Nom de la variable. Obligatoire. |
|**value** <br/> |URL de l’image. Obligatoire. |
|**altText** <br/> |Texte de remplacement à afficher pour l’accessibilité et lorsque l’utilisateur déplace le pointeur de la souris sur l’image. Facultatif. |
|**href** <br/> |Lien hypertexte à utiliser lorsque l’utilisateur clique sur l’image, si la cible souhaitée n’est pas l’URL d’image spécifiée par **l’élément de** valeur. Facultatif. |
   
### <a name="publishervariable"></a>publisherVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Nom de la variable. Obligatoire. |
|**id** <br/> |ID unique de l’utilisateur. Obligatoire. |
|**nameHint** <br/> |Nom à afficher dans l’élément de flux. Facultatif. |
|**profileUrl** <br/> |URL du profil de la personne qui sera utilisée comme lien hypertexte pour le nom de la personne dans l’élément de flux, si le nom de la personne est présent. Facultatif. |
|**emailAddress** <br/> |Adresse de messagerie utilisée pour mettre à jour les informations de contact de cette personne dans Outlook. Facultatif. |
   
### <a name="textvariable"></a>textVariable

|**Élément**|**Description**|
|:-----|:-----|
|**nom** <br/> |Nom de la variable. Obligatoire. |
|**value** <br/> |Texte à afficher. Facultatif. |
   
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du XML pour un élément de flux d’activités](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails, élément](activitydetails-element.md)  
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)  
- [Recommandations en matière d’affichage correct des activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Outlook schéma XML du fournisseur Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

