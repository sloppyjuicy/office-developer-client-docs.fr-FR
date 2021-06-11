---
title: Développement d’un fournisseur TNEF-Enabled transport de données
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 282b1866699b695c647caedd130ce5abc1bcbc2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439001"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Développement d’un fournisseur TNEF-Enabled transport de données

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour promouvoir l’interopérabilité entre les systèmes de messagerie qui assurent la prise en charge de différents ensembles de fonctionnalités MAPI, MAPI fournit le format TNEF (Transport Neutral Encapsulation Format) comme moyen standard de transférer des données. Ce format encapsule les propriétés MAPI non pris en charge par un système de messagerie sous-jacent dans un flux binaire qui peut être transféré avec le message lorsqu’un fournisseur de transport l’envoie. Le fournisseur de transport qui reçoit le message peut ensuite décoder le flux binaire pour récupérer toutes les propriétés du message d’origine et les rendre accessibles aux applications clientes. Le modèle opérationnel pour le TNEF est :
  
- Les clients de messagerie envoient et reçoivent des messages dans un transport TNEF comme d’habitude.
    
- Le transport sépare les propriétés des messages sortants en deux catégories : celles que le système de message sous-jacent prend en charge et celles qui ne le sont pas. Les valeurs des propriétés qui sont pris en charge par le système de messagerie sous-jacent sont converties dans le format requis.
    
- Le transport utilise les méthodes MAPI TNEF pour encoder toutes les propriétés non pris en compte dans un flux de données unique. Le transport transforme ensuite ce flux de données en pièce jointe spéciale sur le message sortant, à l’aide du modèle de pièce jointe du système de messagerie sous-jacent, avant d’envoyer le message.
    
- Un transport TNEF activé qui reçoit un tel message fait deux choses. Tout d’abord, il traduit les propriétés du message entrant (ceux pris en charge par le système de message sous-jacent) en propriétés MAPI. Ensuite, si la pièce jointe spéciale est présente, elle utilise les méthodes MAPI TNEF pour récupérer des propriétés MAPI supplémentaires de la pièce jointe avant de remettre le message à une application cliente.
    
MAPI fournit une implémentation de l’interface **ITnef** à utiliser par les fournisseurs de transport MAPI lors de l’utilisation d’objets TNEF. La [fonction OpenTnefStreamEx permet](opentnefstreamex.md) de créer des objets TNEF et de les associer à un message. Les flux TNEF sont créés au-dessus de l’interface OLE **IStream** 
  
> [!NOTE]
> Vous utilisez **OpenTnefStreamEx pour** créer des objets TNEF. **L’ancienne fonction OpenTnefStream** existe toujours pour la compatibilité avec l’ancien code source et ne doit pas être utilisée dans quelque chose de nouveau. 
  
**L’interface ITnef** fournit les méthodes suivantes : 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Le modèle d’implémentation MAPI TNEF prend en charge :
  
- Toutes les propriétés MAPI sans affecter les autres propriétés de message. Pour que les messages MAPI survit au transport via un système de messagerie, toutes les propriétés qui ne peuvent pas être codées en tant que propriétés du système de messagerie doivent être encapsulées. Étant donné qu’il n’est presque jamais connu au moment de l’envoi d’un message si un client compatible MAPI recevra ou non le message, le schéma d’encapsulation permet à un fournisseur de transport de coder uniquement les propriétés de message MAPI que le système de messagerie ne prend pas en charge en natif. Cela signifie que les messages qui utilisent le TNEF ne sont pas « opaques » pour les systèmes de messagerie qui ne sont pas basés sur MAPI tels que les systèmes de messagerie UNIX SMTP. Ces systèmes reçoivent les propriétés qu’ils prisent en charge, quelle que soit leur manière habituelle, et d’autres propriétés sont reçues en tant que flux de données TNEF codés. Le fournisseur de transport TNEF est responsable de la différenciation entre ces deux ensembles de propriétés et de l’envoi de l’ensemble pris en charge de la manière appropriée pour le système de messagerie. Le TNEF n’effectue aucune hypothèse quant au niveau de prise en charge fourni par un système de messagerie. Toutefois, dans les exemples d’utilisation du TNEF inclus dans cette section, nous partons du principe que le système de messagerie prend en charge au moins une seule pièce jointe en dehors du message. Dans certains cas, la pièce jointe peut uniquement être prise en charge via un flux uuencoded et transmise dans le cadre du texte du message. Ce n’est que dans de très rares cas que le système de messagerie aura si peu de prise en charge des propriétés de message que le codage TNEF complet de toutes les propriétés est nécessaire.
    
- Mécanisme permettant de déterminer si un flux TNEF sur un message entrant appartient au message, en fonction de la propriété MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Cette propriété doit être trouvée à la fois dans le flux TNEF et dans un en-tête de message approprié. Si la propriété a la même valeur aux deux endroits ou s’il est absent à l’un ou l’autre endroit, le flux TNEF est supposé appartenir au message. Sinon, le flux TNEF est ignoré. Les transports TNEF activés sont chargés de choisir une valeur pour cette propriété sur les messages sortants et de l’encoder dans un en-tête de message approprié (par exemple, l’en-tête Message-ID: pour les messages SMTP) et dans le flux TNEF.
    

