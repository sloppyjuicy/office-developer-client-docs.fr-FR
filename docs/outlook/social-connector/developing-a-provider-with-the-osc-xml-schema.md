---
title: Développement d’un fournisseur avec le schéma XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations qui sont transmises à partir d’un réseau social par le biais de fournisseur OSC du réseau à l’OSC.
ms.openlocfilehash: 75809179131ce6c6b8bbe171d2670e59cebe3494
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390547"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Développement d’un fournisseur avec le schéma XML OSC

Le schéma XML du fournisseur Outlook Social Connector (OSC) définit le format d’une quantité importante d’informations qui sont transmises à partir d’un réseau social par le biais de fournisseur OSC du réseau à l’OSC. Le schéma XML permet à un fournisseur OSC spécifier les fonctionnalités du fournisseur, amis, les informations des éléments sur le réseaux sociaux, en utilisant les trois éléments principaux, **fonctionnalités**, **amis**et **activityFeed**et leurs enfants sur les activités éléments. Le fournisseur OSC implémente les interfaces et les méthodes de l’extensibilité de fournisseur OSC, retourner des chaînes de code XML en tant que paramètres de sortie qui respectent le schéma XML du fournisseur OSC. L’OSC appelle ces méthodes pour obtenir des informations qu’il peut comprendre tel que défini par le schéma XML.
  
> [!NOTE]
> Extensibilité du fournisseur OSC prend en charge des fournisseurs de débogage en définissant le `DebugProviders` valeur de la `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` clé de Registre sur 1. Lorsque vous activez le débogage de fournisseur, le OSC valide le fournisseur XML par rapport à la version du schéma XML OSC que vous spécifiez dans l’attribut XML de **xmlns** . Pour OSC 1.1 et les versions de l’OSC depuis Outlook Social Connector 2013, spécifiez l’attribut **xmlns** comme suit :`xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Dans cette section

- [Synchronisation des amis et activités](synchronizing-friends-and-activities.md): décrit les différentes manières que fournisseurs OSC pouvant être synchronisés amis, non amis et des activités sur un réseau social. 
    
- [Exemples de code XML de fournisseur OSC](osc-provider-xml-examples.md): exemples XML inclut qui montrent comment spécifier les fonctionnalités d’un fournisseur OSC, amis et l’activité de flux éléments sur un réseau social à l’aide du schéma XML OSC.
    
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md): explique-méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) qui l’OSC utilise pour obtenir des informations sur les fonctionnalités, exprimées en XML des **fonctionnalités** , à partir du fournisseur OSC. Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC qui autorisent un fournisseur OSC spécifier ses fonctionnalités, y compris son authentifie les utilisateurs et synchronise les amis et les activités. 
    
- [Code XML des amis](xml-for-friends.md): fournit des exemples d’API qui l’OSC utilise pour obtenir des informations de vos amis, exprimées en **amis** XML, à partir du fournisseur OSC. Cette section décrit également les éléments dans le XML **amis** . 
    
- [XML pour les activités](xml-for-activities.md): fournit des exemples d’API qui l’OSC utilise pour obtenir des informations sur des activités, exprimées en **activityFeed** XML, à partir du fournisseur OSC. Cette section décrit également les éléments XML dans le schéma XML du fournisseur OSC autoriser un fournisseur OSC spécifier un flux d’activité. Un flux d’activité inclut le réseau dans lequel les informations sur les activités à l’origine, les éléments de détails de chaque élément d’informations sur les activités (telles que le propriétaire, tapez et date de publication de l’activité) et le modèle pour afficher l’activité. 
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections associées

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [Débogage d'un fournisseur](debugging-a-provider.md)

