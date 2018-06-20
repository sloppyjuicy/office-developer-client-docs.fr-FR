---
title: Vue d’ensemble du code XML pour une activité de flux d’élément
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Un flux d’activité se compose d’une ou plusieurs activités qui ont lieu sur un réseau social. Chaque flux d’activité est représenté par un élément activityFeed et se caractérise par ces trois éléments d’information :'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787718"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Vue d’ensemble du code XML pour une activité de flux d’élément

Un flux d’activité se compose d’une ou plusieurs activités qui ont lieu sur un réseau social. Chaque flux d’activité est représenté par un élément **activityFeed** et se caractérise par ces trois éléments d’information : 
  
- **réseau**: nom du réseau social à partir de laquelle les activités à l’origine.
    
- **activités**: conteneur pour les activités qui se passe sur le compte de l’utilisateur ayant ouvert une session sur ce réseau social.
    
- **modèles**: conteneur pour les modèles utilisés pour afficher les **activités**de l’élément d’activité correspondant.
    
Pour créer un élément de flux d’activités, vous devez vous conformer au schéma XML de l’extensibilité de fournisseur Outlook Social Connector (OSC). La figure 1 montre la que structure XML de l’activité de flux.
  
**La figure 1. Structure XML des informations sur les activités**

![Structure XML d’activité](media/odc_ol14_ta_OSC_Fig06.gif)
  
Pour chaque activité de flux d’élément, les deux composants principaux de ce schéma sont les éléments **activityDetails** et **activityTemplateContainer** : 
  
- L’élément **activityDetails** stocke des informations spécifiques pour chaque activité de flux d’élément, par exemple le nom du propriétaire de l’activité ou l’URL pour les images téléchargées. 
    
- L’élément **activityTemplateContainer** stocke le format ou élément de mise en page pour chaque activité de flux. Il se compose de modèles, représentées par des éléments individuels **activityTemplate** , qui peuvent être réutilisées pour plusieurs éléments de flux. 
    
Pour une activité individuelle flux d’élément, l’élément **activityTemplate** spécifie les quatre éléments d’information suivants : 
  
- **icône**— Spécifie l’URL de l’icône à afficher l’activité de flux d’élément.
    
- **titre**: décrit l’activité de flux item.
    
- **type**: Spécifie le type d’activité, comme un état, photo ou la mise à jour du document.
    
- **données**— spécifie des informations supplémentaires avec un élément de flux d’activités.
    
> [!TIP]
> L’icône affichée dans la flux d’activités est toujours le même que l’icône de fournisseur renvoyée par la propriété **ISocialProvider::SocialNetworkIcon** . 
  
Consultez les rubriques suivantes pour plus d’informations sur l’élément **activityDetails** , l’élément **activityTemplateContainer** , jetons de modèle et variables de modèle : 
  
- [activityDetails, élément](activitydetails-element.md)
    
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
- [Conseils pour l’affichage correctement les activités](guidelines-for-properly-displaying-activities.md)
    
Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Voir aussi

- [XML pour les activités](xml-for-activities.md) 
- [Fournisseur Outlook Social Connector schéma XML](outlook-social-connector-provider-xml-schema.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

