---
title: Développement d’un fournisseur avec le schéma XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d'une quantité importante d'informations transmises à partir d'un réseau social via le fournisseur OSC du réseau au OSC.
ms.openlocfilehash: 75809179131ce6c6b8bbe171d2670e59cebe3494
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281075"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Développement d’un fournisseur avec le schéma XML OSC

Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d'une quantité importante d'informations transmises à partir d'un réseau social via le fournisseur OSC du réseau au OSC. Le schéma XML permet à un fournisseur OSC de spécifier les fonctionnalités du fournisseur, des amis et des éléments du flux d'activités sur le réseau social, en utilisant les trois principaux éléments, **fonctionnalités**, **amis**et **activityFeed**, ainsi que leurs enfants. composants. Le fournisseur OSC implémente les interfaces et leurs méthodes dans l'extensibilité du fournisseur OSC, en renvoyant des chaînes XML comme paramètres de sortie conformes au schéma XML du fournisseur OSC. Le OSC appelle ces méthodes pour obtenir des informations qu'il peut comprendre comme défini par le schéma XML.
  
> [!NOTE]
> L'extensibilité du fournisseur OSC prend en charge le débogage `DebugProviders` des fournisseurs en `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` définissant la valeur de la clé de Registre sur 1. Lorsque vous activez le débogage des fournisseurs, le OSC valide le fournisseur XML par rapport à la version du schéma XML OSC que vous spécifiez dans l'attribut XML **xmlns** . Pour OSC 1,1 et les versions du OSC depuis Outlook Social Connector 2013, spécifiez l'attribut **xmlns** comme suit:`xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Contenu de cette section

- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md): décrit les différentes façons dont les fournisseurs OSC peuvent synchroniser des amis, des non-amis et des activités sur un réseau social. 
    
- [Exemples de fournisseurs XML OSC](osc-provider-xml-examples.md): inclut des exemples XML qui montrent comment spécifier les fonctionnalités d'un fournisseur OSC, des amis et des éléments de flux d'activité sur un réseau social à l'aide du schéma XML OSC.
    
- [XML pour les fonctionnalités](xml-for-capabilities.md): explique la méthode- [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) que OSC utilise pour obtenir des informations sur les fonctionnalités, exprimées dans les **fonctionnalités** XML, à partir du fournisseur OSC. Cette section décrit également les éléments XML du schéma XML du fournisseur OSC qui permettent à un fournisseur OSC de spécifier sa fonctionnalité, notamment comment il authentifie les utilisateurs et synchronise les amis et les activités. 
    
- [XML pour les amis](xml-for-friends.md): donne des exemples d'API que le OSC utilise pour obtenir des informations sur les amis, exprimées dans des **amis** XML, à partir du fournisseur OSC. Cette section décrit également les éléments du **** XML Friends. 
    
- [XML pour les activités](xml-for-activities.md): donne des exemples d'API que le OSC utilise pour obtenir des informations sur les activités, exprimées dans **activityFeed** XML, à partir du fournisseur OSC. Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC qui permettent à un fournisseur OSC de spécifier un flux d'activités. Un flux d'activités comprend le réseau sur lequel les éléments du flux d'activités sont issus, les détails de chaque élément de flux d'activité (par exemple, le propriétaire, le type et la date de publication de l'activité), ainsi que le modèle d'affichage de l'activité. 
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections connexes

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  
- [Meilleures pratiques pour le développement d'un fournisseur](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [Débogage d'un fournisseur](debugging-a-provider.md)

