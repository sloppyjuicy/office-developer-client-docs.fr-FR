---
title: Débogage d’un fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC) :'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281068"
---
# <a name="debugging-a-provider"></a>Débogage d’un fournisseur

Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC) : 
  
- À l’aide des commandes de débogage dans le composant ruban de l’interface utilisateur Office Fluent dans Outlook ou de l’application cliente Office de prise en charge pour que l’OSC prenne différentes mesures.
    
- Utilisation de Fiddler pour suivre les appels d’API et le XML envoyés entre un réseau social et son fournisseur OSC
    
## <a name="debug-buttons"></a>Boutons de débogage

L’extensibilité du fournisseur OSC permet de déboguer un fournisseur OSC. Pour déboguer un fournisseur, créez une valeur de type DWORD dans le Registre Windows sous la clé (comme illustré dans la ligne suivante) et définissez la valeur sur `DebugProviders` `SocialConnector` `DebugProviders` 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Par défaut, le débogage du fournisseur est hors service. Si la valeur n’est pas présente, ou si elle est présente et définie sur la valeur 0, le débogage du fournisseur  `DebugProviders` est désactivé. 
  
Si le débogage du fournisseur est allumé, l’OSC affiche une boîte de dialogue d’alerte avec des informations détaillées sur les erreurs lorsqu’une erreur se produit et valide tout XML de fournisseur OSC par rapport au schéma XML du fournisseur OSC. En fonction de l’espace de noms spécifié pour une chaîne XML, un fournisseur OSC développé à l’aide d’OSC 1.0 est validé par rapport au fichier de schéma OSC 1.0, OutlookSocialProvider.xsd. Un fournisseur OSC développé à l’aide d’OSC 1.1 ou ultérieur est validé par rapport au fichier de schéma, OutlookSocialProvider_1.1.xsd. Lorsque vous utilisez la valeur, l’alerte de débogage s’affiche pour tous les fournisseurs chargés au lieu  `DebugProviders` d’un fournisseur spécifique. 
  
Pour afficher les boutons de débogage qui peuvent vous aider à déboguer un fournisseur, créez une valeur de type DWORD dans le Registre Windows sous la clé et définissez la valeur sur `ShowDebugButtons` `SocialConnector` `ShowDebugButtons` 1. Pour masquer les boutons de barre de commandes de débogage, définissez  `ShowDebugButtons` la valeur sur 0. 
  
Pour Outlook 2010 et les applications clientes depuis Office 2013, les  boutons de débogage apparaissent sous l’onglet Des applications du ruban de l’explorateur. Pour Outlook 2007 et Outlook 2003, les boutons de débogage apparaissent dans la barre de commandes standard de la fenêtre Outlook’explorateur. 
  
Le tableau suivant décrit les boutons de débogage.
  
|**Bouton Déboguer**|**Fonction**|
|:-----|:-----|
|Synchroniser les contacts  <br/> |Fait que l’OSC demande uniquement au fournisseur OSC les contacts mis en cache.  <br/> |
|Synchronisation de laxisme  <br/> |Indique à OSC de remplir les données de la Exchange d’adresses globale pour Outlook contacts.  <br/> |
|Invalider le cache de catégories  <br/> |Entraîne le rechargement par OSC de la liste des catégories pour chaque magasin lors de l’actualisation du flux d’activités.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler est un outil de débogage over-the-wire pour vérifier les appels d’API envoyés par votre fournisseur au réseau social et le XML envoyé par le réseau social à votre fournisseur. Fiddler est disponible en téléchargement sur [fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Voir aussi

- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md) 
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

