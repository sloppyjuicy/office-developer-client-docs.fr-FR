---
title: Débogage d’un fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281068"
---
# <a name="debugging-a-provider"></a>Débogage d’un fournisseur

Il existe plusieurs façons de déboguer un fournisseur Outlook Social Connector (OSC): 
  
- À l'aide des commandes de débogage dans le composant de ruban de l'interface utilisateur Office Fluent dans Outlook ou de l'application cliente Office de prise en charge, la commande OSC doit prendre différentes actions.
    
- En utilisant Fiddler pour suivre les appels d'API et le code XML envoyé entre un réseau social et son fournisseur OSC
    
## <a name="debug-buttons"></a>Boutons de déBogage

L'extensibilité du fournisseur OSC permet de déboguer un fournisseur OSC. Pour déboguer un fournisseur, `DebugProviders` créez une valeur de type DWORD dans le Registre Windows `SocialConnector` sous la clé (comme indiqué dans la ligne suivante), et `DebugProviders` définissez la valeur sur 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Par défaut, le débogage du fournisseur est désactivé. Si la `DebugProviders` valeur n'est pas présente, ou si elle est présente et définie sur 0, le débogage du fournisseur est désactivé. 
  
Si le débogage du fournisseur est activé, le OSC affiche une boîte de dialogue d'alerte avec des informations détaillées sur l'erreur lorsqu'une erreur se produit et valide les fournisseurs OSC XML par rapport au schéma XML du fournisseur OSC. En fonction de l'espace de noms spécifié pour une chaîne XML, un fournisseur OSC développé à l'aide de OSC 1,0 est validé par rapport au fichier de schéma OSC 1,0, OutlookSocialProvider. xsd. Un fournisseur OSC développé à l'aide de OSC 1,1 ou version ultérieure est validé par rapport au fichier de schéma OutlookSocialProvider_ 1.1. xsd. Lorsque vous utilisez la `DebugProviders` valeur, l'alerte de débogage apparaît pour tous les fournisseurs chargés au lieu d'un fournisseur spécifique. 
  
Pour afficher les boutons de débogage qui peuvent vous aider à déboguer un fournisseur, créez une `ShowDebugButtons` valeur de type DWORD `SocialConnector` dans le Registre Windows sous `ShowDebugButtons` la clé, et définissez la valeur sur 1. Pour masquer les boutons de la barre de commandes de `ShowDebugButtons` débogage, définissez la valeur sur 0. 
  
Pour Outlook 2010 et les applications clientes depuis Office 2013, les boutons de débogage apparaissent sous l'onglet **compléments** du ruban Explorateur. Pour Outlook 2007 et Outlook 2003, les boutons de débogage apparaissent sur la barre de commandes standard de la fenêtre de l'explorateur Outlook. 
  
Le tableau suivant décrit les boutons de débogage.
  
|**Bouton déBogage**|**Fonction**|
|:-----|:-----|
|Synchroniser les contacts  <br/> |Indique à l'OSC de demander au fournisseur OSC les contacts mis en cache uniquement.  <br/> |
|Synchronisation de la liste d'adresses globale  <br/> |Permet à OSC de remplir les données de la liste d'adresses globale d'Exchange vers les contacts Outlook.  <br/> |
|Cache de catégorie Invalidate  <br/> |La méthode OSC charge de nouveau la liste de catégories pour chaque banque lorsque le flux d'activités est actualisé.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler est un outil de débogage par câble permettant de vérifier les appels d'API envoyés par votre fournisseur au réseau social, ainsi que le code XML envoyé par le réseau social à votre fournisseur. Fiddler peut être téléchargé sur le [proxy de débogage Web Fiddler](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Voir aussi

- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md) 
- [Meilleures pratiques pour le développement d'un fournisseur](best-practices-for-developing-a-provider.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

