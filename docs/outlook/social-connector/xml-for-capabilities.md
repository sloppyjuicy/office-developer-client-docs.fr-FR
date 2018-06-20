---
title: Fichier XML pour les fonctionnalités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'L’élément capabilities dans le schéma XML du fournisseur (OSC) permet à un fournisseur OSC spécifier ses fonctionnalités. Ces fonctionnalités sont les suivantes :'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787707"
---
# <a name="xml-for-capabilities"></a>Fichier XML pour les fonctionnalités

L’élément **capabilities** dans le schéma XML du fournisseur (OSC) permet à un fournisseur OSC spécifier ses fonctionnalités. Ces fonctionnalités sont les suivantes : 
  
- Si le fournisseur prend en charge l’obtention, la mise en cache ou recherchez dynamiquement des amis et des activités à partir du réseau social.
    
- Comment l’OSC doit afficher certaines des interfaces utilisateur d’ouverture de session.
    
- Si l’OSC doit utiliser l’authentification basée sur les formulaires ou configurer automatiquement les réseaux sociaux et les journaux de l’utilisateur sur le réseau social.
    
Le schéma XML pour les **fonctionnalités** d’est essentiel car il identifie l’OSC les fonctionnalités prises en charge par le fournisseur. Un fournisseur OSC doit implémenter la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) qui renvoie une chaîne de _résultat_ . L’OSC appelle **ISocialProvider::GetCapabilities** pour obtenir des informations sur les fonctionnalités du fournisseur OSC dans la chaîne de _résultat_ , qui est conforme à la définition de schéma XML pour l’élément **capabilities** . Ces informations permettent les appels suivants à partir de l’OSC au fournisseur OSC fonctionner correctement. 
  
Pour spécifier les fonctionnalités d’un fournisseur OSC comme paramètre de sortie de la méthode **ISocialProvider::GetCapabilities** , vous devez vous conformer au schéma XML OSC fournisseur extensibilité. La figure suivante illustre la structure XML des **capacités** . 
  
**La figure 1. \<fonctionnalités\> structure XML**

![Structure XML des fonctionnalités](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Pour obtenir des descriptions détaillées des éléments enfants de l’élément de **fonctionnalités** , voir [Fonctionnalités des éléments XML](capabilities-xml-elements.md). Pour obtenir un exemple de **fonctionnalités** XML, voir [Exemple de code XML des capacités](capabilities-xml-example.md). Pour une définition complète du schéma XML de fournisseur OSC, y compris les éléments qui sont obligatoires ou facultatives, voir [Schéma du XML fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Voir aussi

- [Exemple de code XML des fonctionnalités](capabilities-xml-example.md)  
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md)  
- [Code XML des amis](xml-for-friends.md)  
- [XML pour les activités](xml-for-activities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

