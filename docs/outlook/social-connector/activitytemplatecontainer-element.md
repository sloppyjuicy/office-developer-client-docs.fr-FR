---
title: activityTemplateContainer, élément
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un élément activityTemplateContainer est un modèle qui vous permet de mettre en forme les éléments d’informations sur les activités et la réutilisation XML qui spécifie une mise en forme.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787582"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer, élément

Un élément **activityTemplateContainer** est un modèle qui vous permet de mettre en forme les éléments d’informations sur les activités et la réutilisation XML qui spécifie une mise en forme. Utilisez l’ID (**applicationID** et **templateID**) pour correspondre à un élément de flux (**activityDetails**) à un modèle (**activityTemplateContainer**). Stocker les données de mise en page dans le cadre de l’élément **activityTemplate** . Pour référencer des données sont extraites de l’activité individuelle flux élément, utilisez variables de modèle comme espaces réservés pour des informations telles que des personnes, des liens et le texte. 
  
Le tableau suivant décrit les trois éléments nécessitant l’élément **activityTemplateContainer** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**applicationID** <br/> |Une des deux identificateurs uniques qui sont utilisés pour la correspondance de l’élément de flux avec son modèle. Si vous disposez de plusieurs applications ou autres groupes, il peut servir en tant qu’un organisateur de modèle de premier niveau.  <br/> |
|**templateID** <br/> |Second ID unique qui est utilisée pour la correspondance de l’élément à son modèle de flux. Cela peut servir d’un organisateur de modèle de second niveau.  <br/> |
|**activityTemplate** <br/> |La mise en page du modèle (éléments de **données** , le **titre**et**icône**) et le type d’activité (**type** d’élément).  <br/> |
   
Le tableau suivant décrit les éléments enfants **activityTemplate**, qui décrivent la mise en page et le type d’un modèle.
  
|**Élément**|**Description**|
|:-----|:-----|
|**icon** <br/> |Un jeton de liaison, qui fait référence à l’URL de l’icône de cet élément de flux.  <br/> |
|**title** <br/> |Les informations requises pour l’élément de flux.  <br/> |
|**type** <br/> |Le type d’activité, par exemple une mise à jour d’état, photo ou document.  <br/> |
|**data** <br/> |Des informations supplémentaires pour l’élément de flux, tels que des images, du texte ou des liens.  <br/> |
   
Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du code XML pour une activité de flux d’élément](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails, élément](activitydetails-element.md)  
- [Variables de modèle](template-variables.md)  
- [Conseils pour l’affichage correctement les activités](guidelines-for-properly-displaying-activities.md)  
- [XML pour les activités](xml-for-activities.md)  
- [Fournisseur Outlook Social Connector schéma XML](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

