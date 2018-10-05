---
title: Débogage d’un fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Il existe plusieurs façons, vous pouvez déboguer un fournisseur Outlook Social Connector (OSC) :'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386851"
---
# <a name="debugging-a-provider"></a>Débogage d’un fournisseur

Il existe plusieurs façons, vous pouvez déboguer un fournisseur Outlook Social Connector (OSC) : 
  
- À l’aide de commandes de débogage dans le composant du ruban de l’interface utilisateur Office Fluent dans Outlook ou l’application Office cliente prise en charge de provoquer l’OSC effectuer des actions différentes.
    
- À l’aide de Fiddler pour l’API de suivi des appels et XML envoyés entre un réseau social et son fournisseur OSC
    
## <a name="debug-buttons"></a>Déboguer les boutons

L’extensibilité du fournisseur OSC offre la possibilité de débogage d’un fournisseur OSC. Pour déboguer un fournisseur, créez un `DebugProviders` une valeur de type DWORD dans le Registre Windows sous la `SocialConnector` clé (comme indiqué dans la ligne suivante) et définir le `DebugProviders` la valeur 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Par défaut, le fournisseur de débogage est désactivé. Si le `DebugProviders` valeur n’est pas présente, ou il est présent et défini sur une valeur de 0, le fournisseur de débogage est désactivé. 
  
Si le fournisseur de débogage est activé, le OSC affiche une boîte de dialogue d’alerte avec des informations d’erreur détaillé lorsqu’une erreur se produit et valide tout fournisseur OSC XML par rapport au schéma XML du fournisseur OSC. En fonction de l’espace de noms spécifié pour une chaîne XML, un fournisseur OSC développé à l’aide de OSC 1.0 est validé par rapport au fichier de schéma 1.0 OSC, OutlookSocialProvider.xsd. Un fournisseur OSC développées à l’aide de OSC 1.1 ou ultérieure est validé par rapport au fichier de schéma, OutlookSocialProvider_1.1.xsd. Lorsque vous utilisez la `DebugProviders` valeur, l’alerte de débogage s’affiche pour les fournisseurs tous chargés au lieu d’un fournisseur spécifique. 
  
Pour afficher les boutons de débogage qui peuvent vous aider à déboguer un fournisseur, créez un `ShowDebugButtons` une valeur de type DWORD dans le Registre Windows sous la `SocialConnector` clé et définir le `ShowDebugButtons` la valeur 1. Pour masquer les boutons de barre de commande debug, définissez la `ShowDebugButtons` valeur à 0. 
  
Pour Outlook 2010 et les applications clientes par rapport à Office 2013, les boutons de débogage apparaissent sous l’onglet **compléments** du ruban de l’Explorateur de solutions. Pour Outlook 2007 et Outlook 2003, les boutons de débogage apparaissent dans la barre de commande standard de la fenêtre d’Explorateur. 
  
Le tableau suivant décrit les boutons de débogage.
  
|**Bouton de débogage**|**Fonction**|
|:-----|:-----|
|Synchroniser les Contacts  <br/> |Entraîne l’OSC demander le fournisseur OSC uniquement les contacts mis en cache.  <br/> |
|Synchronisation de liste d’adresses globale  <br/> |Entraîne l’OSC remplir des données à partir de la liste d’adresses globale Exchange aux contacts Outlook.  <br/> |
|Invalider le Cache de catégorie  <br/> |Entraîne l’OSC recharger la liste des catégories pour chaque banque lorsque le flux d’activité est actualisé.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler est un outil de débogage over-the-wire pour vérifier les appels d’API envoyés par votre fournisseur au réseau social et XML envoyées par le réseaux sociaux à votre fournisseur. Fiddler est disponible pour téléchargement à l’adresse [Proxy de débogage Web Fiddler](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Voir aussi

- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md) 
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

