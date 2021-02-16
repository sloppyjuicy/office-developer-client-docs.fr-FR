---
title: Développement d’un fournisseur avec le schéma XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations transmises d’un réseau social via le fournisseur OSC du réseau à OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539254"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Développement d’un fournisseur avec le schéma XML OSC

Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations transmises d’un réseau social via le fournisseur OSC du réseau à OSC. Le schéma XML permet à un fournisseur OSC de spécifier les fonctionnalités du fournisseur, des amis et des éléments de flux d’activités sur le réseau social, à l’aide des trois éléments **principaux,** fonctionnalités **,** amis et **activityFeed** et leurs éléments enfants. Le fournisseur OSC implémente des interfaces et leurs méthodes dans l’extensibilité du fournisseur OSC, renvoyant des chaînes XML en tant que paramètres de sortie conformes au schéma XML du fournisseur OSC. L’OSC appelle ces méthodes pour obtenir des informations qu’il peut comprendre telles que définies par le schéma XML.
  
> [!NOTE]
> L’extensibilité du fournisseur OSC prend en charge le débogage des fournisseurs en fixant la valeur de la clé de Registre `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` sur 1. Lorsque vous activer le débogage de fournisseur, l’OSC valide le XML du fournisseur par rapport à la version du schéma XML OSC que vous spécifiez dans l’attribut XML **xmlns.** Pour OSC 1.1 et les versions de l’OSC depuis Outlook Social Connector 2013, spécifiez l’attribut **xmlns** comme suit : `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Contenu de cette section

- [Synchronisation des amis et](synchronizing-friends-and-activities.md)des activités : décrit les différentes façons dont les fournisseurs OSC peuvent synchroniser des amis, des amis et des activités sur un réseau social. 
    
- Exemples XML de fournisseur OSC : inclut des exemples XML qui montrent comment spécifier les fonctionnalités d’un fournisseur [OSC,](osc-provider-xml-examples.md)des amis et des éléments de flux d’activités sur un réseau social à l’aide du schéma XML OSC.
    
- [XML pour](xml-for-capabilities.md)les fonctionnalités : explique la méthode [- ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que l’OSC utilise pour obtenir des informations sur les fonctionnalités, exprimées en **XML** de fonctionnalités, auprès du fournisseur OSC. Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC qui permettent à un fournisseur OSC de spécifier ses fonctionnalités, y compris la façon dont il authentifier les utilisateurs et synchronise les amis et les activités. 
    
- [XML pour les](xml-for-friends.md)amis : donne des exemples d’API que l’OSC utilise pour obtenir les informations des amis, exprimées en **XML** d’amis, auprès du fournisseur OSC. Cette section décrit également les éléments du XML **amis.** 
    
- [XML pour](xml-for-activities.md)les activités : donne des exemples d’API que l’OSC utilise pour obtenir des informations sur les activités, exprimées dans **activityFeed** XML, auprès du fournisseur OSC. Cette section décrit également les éléments XML du schéma XML du fournisseur OSC qui permettent à un fournisseur OSC de spécifier un flux d’activités. Un flux d’activités inclut le réseau d’origine des éléments de flux d’activités, les détails de chaque élément de flux d’activités (par exemple, propriétaire, type et date de publication de l’activité) et le modèle d’affichage de l’activité. 
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections connexes

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [Débogage d'un fournisseur](debugging-a-provider.md)

