---
title: Élément activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un élément activityTemplateContainer est un modèle qui vous permet de mettre en forme vos éléments de flux d'activités et de réutiliser du code XML qui spécifie une mise en page.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281119"
---
# <a name="activitytemplatecontainer-element"></a>Élément activityTemplateContainer

Un élément **activityTemplateContainer** est un modèle qui vous permet de mettre en forme vos éléments de flux d'activités et de réutiliser du code XML qui spécifie une mise en page. Utilisez les ID (**ApplicationID** et **TemplateID**) pour faire correspondre un élément de flux (**activityDetails**) à un modèle (**activityTemplateContainer**). Stockez les données de disposition dans le cadre de l'élément **ActivityTemplate** . Pour référencer des données qui sont extraites de l'élément de flux d'activités individuel, utilisez des variables de modèle comme espaces réservés pour des informations telles que des personnes, des liens et du texte. 
  
Le tableau suivant décrit les trois éléments requis par l'élément **activityTemplateContainer** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**applicationID** <br/> |Un des deux ID uniques qui sont utilisés pour faire correspondre l'élément de flux à son modèle. Si vous avez plusieurs applications ou autres groupements, il peut être utilisé en tant qu'organisateur de modèles de premier niveau.  <br/> |
|**templateID** <br/> |Deuxième ID unique utilisé pour faire correspondre l'élément de flux à son modèle. Il peut être utilisé en tant qu'organisateur de modèles de second niveau.  <br/> |
|**activityTemplate** <br/> |La disposition du modèle (**icône**, **titre**et éléments de **données** ) et le type d'activité (élément**type** ).  <br/> |
   
Le tableau suivant décrit les éléments enfants de **ActivityTemplate**, qui décrivent la mise en page et le type d'un modèle.
  
|**Élément**|**Description**|
|:-----|:-----|
|**icon** <br/> |Un jeton de liaison, qui fait référence à l'URL de l'icône de cet élément de flux.  <br/> |
|**title** <br/> |Informations requises pour l'élément de flux.  <br/> |
|**type** <br/> |Type d'activité, par exemple une mise à jour de l'État, de la photo ou du document.  <br/> |
|**data** <br/> |Informations supplémentaires pour l'élément de flux, telles que des images, du texte ou des liens.  <br/> |
   
Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML de flux d'activités](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble du code XML pour un élément de flux d'activité](overview-of-xml-for-an-activity-feed-item.md)  
- [Élément activityDetails](activitydetails-element.md)  
- [Variables de modèle](template-variables.md)  
- [Instructions pour afficher correctement les activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

