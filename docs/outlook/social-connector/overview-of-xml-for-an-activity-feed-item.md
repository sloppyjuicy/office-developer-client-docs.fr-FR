---
title: Vue d’ensemble du code XML pour un élément de flux d’activité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Un flux d’activités se compose d’une ou de plusieurs activités se produisant sur un réseau social. Chaque flux d’activités est représenté par un élément activityFeed et se caractérise par ces trois éléments d’informations :'
ms.openlocfilehash: 528a7e2c32c7a5c4c2947bfad864accd92fcc419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566114"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Vue d’ensemble du code XML pour un élément de flux d’activité

Un flux d’activités se compose d’une ou de plusieurs activités se produisant sur un réseau social. Chaque flux d’activités est représenté par un **élément activityFeed** et se caractérise par ces trois éléments d’informations : 
  
- **réseau**— Nom du réseau social d’où proviennent les activités.
    
- **activités :** conteneur pour les activités qui se produisent sur le compte de l’utilisateur connecté sur ce réseau social.
    
- **modèles :** conteneur pour les modèles utilisés pour afficher l’élément d’activité correspondant dans **les activités.**
    
Pour créer un élément de flux d’activités, vous devez vous conformer au schéma XML d’extensibilité du Outlook Social Connector (OSC). La figure 1 illustre la structure XML du flux d’activités.
  
**Figure 1. Structure XML du flux d’activités**

![Structure XML d’activité](media/odc_ol14_ta_OSC_Fig06.gif)
  
Pour chaque élément de flux d’activités, les deux éléments les plus importants de ce schéma sont les éléments **activityDetails** et **activityTemplateContainer** : 
  
- **L’élément activityDetails** stocke des informations spécifiques pour chaque élément de flux d’activités, telles que le nom du propriétaire de l’activité ou l’URL des images téléchargées. 
    
- **L’élément activityTemplateContainer stocke** le format ou la disposition de chaque élément de flux d’activités. Il se compose de modèles, représentés par des éléments **activityTemplate** individuels, qui peuvent être réutilisés pour plusieurs éléments de flux. 
    
Pour un élément de flux d’activités individuel, **l’élément activityTemplate** spécifie les quatre éléments d’informations suivants : 
  
- **icône**: spécifie l’URL de l’icône pour afficher l’élément de flux d’activités.
    
- **titre**— Décrit l’élément de flux d’activités.
    
- **type**: spécifie le type d’activité, tel qu’une mise à jour d’état, de photo ou de document.
    
- **données**: spécifie toutes les informations supplémentaires affichées avec l’élément de flux d’activités.
    
> [!TIP]
> L’icône affichée dans le flux d’activités est toujours la même que l’icône de fournisseur renvoyée par la propriété **ISocialProvider::SocialNetworkIcon.** 
  
Consultez les rubriques suivantes pour plus d’informations sur l’élément **activityDetails,** l’élément **activityTemplateContainer,** les jetons de modèle et les variables de modèle : 
  
- [activityDetails, élément](activitydetails-element.md)
    
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
- [Recommandations en matière d’affichage correct des activités](guidelines-for-properly-displaying-activities.md)
    
Pour obtenir un exemple de données XML de flux d’activités, voir [l’exemple XML des flux d’activités.](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Voir aussi

- [XML pour les activités](xml-for-activities.md) 
- [Outlook Schéma XML du fournisseur Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

