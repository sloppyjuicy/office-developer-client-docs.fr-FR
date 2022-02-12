---
title: activityTemplateContainer, élément
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un élément activityTemplateContainer est un modèle qui vous permet de mettre en forme vos éléments de flux d’activités et de réutiliser le code XML qui spécifie une disposition.
ms.openlocfilehash: 6546e91112b31f3751a04242b7851841f7740f3e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770660"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer, élément

Un **élément activityTemplateContainer** est un modèle qui vous permet de mettre en forme vos éléments de flux d’activités et de réutiliser le code XML qui spécifie une disposition. Utilisez des ID (**applicationID** et **templateID**) pour faire correspondre un élément de flux (**activityDetails**) à un modèle (**activityTemplateContainer**). Stockez les données de disposition dans le cadre de **l’élément activityTemplate** . Pour référencer des données qui sont tirées de l’élément de flux d’activités individuel, utilisez des variables de modèle comme espaces réservé pour des informations telles que des personnes, des liens et du texte. 
  
Le tableau suivant décrit les trois éléments nécessaires à **l’élément activityTemplateContainer** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**applicationID** <br/> |L’un des deux ID uniques utilisés pour faire correspondre l’élément de flux à son modèle. Si vous avez plusieurs applications ou d’autres regroupements, vous pouvez l’utiliser comme organisateur de modèles de premier niveau. |
|**templateID** <br/> |Deuxième ID unique utilisé pour faire correspondre l’élément de flux à son modèle. Il peut être utilisé en tant qu’organisateur de modèles de second niveau. |
|**activityTemplate** <br/> |La disposition du modèle (éléments **d’icône**, **de titre** et de données) et le type d’activité (**élément de type**). |
   
Le tableau suivant décrit les éléments enfants de **activityTemplate**, qui décrivent la disposition et le type d’un modèle.
  
|**Élément**|**Description**|
|:-----|:-----|
|**icon** <br/> |Jeton de lien, qui fait référence à l’URL de l’icône pour cet élément de flux. |
|**title** <br/> |Informations requises pour l’élément de flux. |
|**type** <br/> |Type d’activité, tel qu’une mise à jour de l’état, d’une photo ou d’un document. |
|**data** <br/> |Toute information supplémentaire pour l’élément de flux, telles que des images, du texte ou des liens. |
   
Pour obtenir un exemple de données XML de flux d’activités, voir [l’exemple XML des flux d’activités](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du XML pour un élément de flux d’activités](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails, élément](activitydetails-element.md)  
- [Variables de modèle](template-variables.md)  
- [Recommandations en matière d’affichage correct des activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Outlook schéma XML du fournisseur Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

