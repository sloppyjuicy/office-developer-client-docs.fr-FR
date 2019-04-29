---
title: Vue d’ensemble du code XML pour un élément de flux d’activité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: "Un flux d'activités se compose d'une ou de plusieurs activités se produisant sur un réseau social. Chaque flux d'activité est représenté par un élément activityFeed et se caractérise par ces trois éléments d'information:"
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439946"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Vue d’ensemble du code XML pour un élément de flux d’activité

Un flux d'activités se compose d'une ou de plusieurs activités se produisant sur un réseau social. Chaque flux d'activité est représenté par un élément **activityFeed** et se caractérise par ces trois éléments d'information: 
  
- **réseau**: nom du réseau social à l'origine des activités.
    
- **activités**: conteneur pour les activités se produisant sur le compte de l'utilisateur connecté sur ce réseau social.
    
- **Templates**: conteneur pour les modèles qui sont utilisés pour afficher l'élément d'activité correspondant dans les **activités**.
    
Pour créer un élément de flux d'activités, vous devez vous conformer au schéma XML de l'extensibilité du fournisseur Outlook Social Connector (OSC). La figure 1 illustre la structure XML de flux d'activités.
  
**Figure 1. Structure XML des informations sur les activités**

![Structure XML d’activité](media/odc_ol14_ta_OSC_Fig06.gif)
  
Pour chaque élément de flux d'activités, les deux parties les plus importantes de ce schéma sont les éléments **activityDetails** et **activityTemplateContainer** : 
  
- L'élément **activityDetails** stocke des informations spécifiques pour chaque élément de flux d'activité, telles que le nom du propriétaire de l'activité ou l'URL des images chargées. 
    
- L'élément **activityTemplateContainer** stocke le format ou la mise en page de chaque élément de flux d'activité. Elle se compose de modèles, représentés par des éléments **ActivityTemplate** individuels, qui peuvent être réutilisés pour plusieurs éléments de flux. 
    
Pour un élément de flux d'activités individuel, l'élément **ActivityTemplate** spécifie les quatre éléments d'information suivants: 
  
- **Icon**— spécifie l'URL de l'icône qui affiche l'élément de flux d'activités.
    
- **titre**— décrit l'élément de flux d'activités.
    
- **type**— spécifie le type d'activité, par exemple un État, une photo ou une mise à jour de document.
    
- **Data**— spécifie toutes les informations supplémentaires affichées avec l'élément de flux d'activité.
    
> [!TIP]
> L'icône affichée dans le flux d'activités est toujours identique à l'icône du fournisseur renvoyée par la propriété **ISocialProvider:: SocialNetworkIcon** . 
  
Pour plus d'informations sur l'élément **activityDetails** , l'élément **activityTemplateContainer** , les jetons de modèle et les variables de modèle, consultez les rubriques suivantes: 
  
- [Élément activityDetails](activitydetails-element.md)
    
- [Élément activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
- [Instructions pour afficher correctement les activités](guidelines-for-properly-displaying-activities.md)
    
Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML](activity-feed-xml-example.md)d'informations sur les activités.
  
## <a name="see-also"></a>Voir aussi

- [XML pour les activités](xml-for-activities.md) 
- [Schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

