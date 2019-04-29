---
title: XML pour les fonctionnalités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: "L'élément Capabilities dans le schéma XML du fournisseur (OSC) permet à un fournisseur OSC de spécifier sa fonctionnalité. Cette fonctionnalité inclut les éléments suivants:"
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435004"
---
# <a name="xml-for-capabilities"></a>XML pour les fonctionnalités

L'élément **Capabilities** dans le schéma XML du fournisseur (OSC) permet à un fournisseur OSC de spécifier sa fonctionnalité. Cette fonctionnalité inclut les éléments suivants: 
  
- Si le fournisseur prend en charge l'obtention, la mise en cache ou la recherche dynamique des amis et des activités à partir du réseau social.
    
- Comment le OSC doit afficher certaines interfaces utilisateur d'ouverture de session.
    
- Si OSC doit utiliser l'authentification basée sur les formulaires ou configurez automatiquement le réseau social et connectez-vous à l'utilisateur sur le réseau social.
    
Le schéma XML pour les **fonctionnalités** est essentiel, car il identifie au OSC les fonctionnalités prises en charge par le fournisseur. Un fournisseur OSC doit implémenter la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) qui renvoie une chaîne de _résultat_ . Le OSC appelle **ISocialProvider:: GetCapabilities** pour obtenir des informations sur les fonctionnalités du fournisseur OSC dans la chaîne de _résultat_ , qui est conforme à la définition de schéma XML pour l'élément **Capabilities** . Ces informations permettent aux appels suivants de OSC vers le fournisseur OSC de fonctionner correctement. 
  
Pour spécifier les fonctionnalités d'un fournisseur OSC en tant que paramètre de sortie de la méthode **ISocialProvider:: GetCapabilities** , vous devez vous conformer au schéma XML de l'extensibilité du fournisseur OSC. La figure suivante illustre la structure XML des **fonctionnalités** . 
  
**Figure 1. \<structure\> XML des fonctionnalités**

![Structure XML des fonctionnalités](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Pour obtenir une description détaillée des éléments enfants de l'élément **Capabilities** , voir [Capabilities XML Elements](capabilities-xml-elements.md). Pour obtenir un exemple de code XML de **fonctionnalités** , consultez la rubrique [Capabilities XML example](capabilities-xml-example.md). Pour obtenir une définition complète du schéma XML du fournisseur OSC, y compris les éléments requis ou facultatifs, voir [schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Voir aussi

- [Exemple de XML de fonctionnalités](capabilities-xml-example.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)  
- [XML pour les amis](xml-for-friends.md)  
- [XML pour les activités](xml-for-activities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

