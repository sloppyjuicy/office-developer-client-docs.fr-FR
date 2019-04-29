---
title: Développement d'un fournisseur de transport compatible TNEF
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
# <a name="developing-a-tnef-enabled-transport-provider"></a>Développement d'un fournisseur de transport compatible TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour promouvoir l'interopérabilité entre les systèmes de messagerie qui prennent en charge différents ensembles de fonctionnalités MAPI, MAPI fournit le format TNEF (Transport Neutral Encapsulation Format) comme moyen standard de transfert de données. Ce Format encapsule les propriétés MAPI qui ne sont pas prises en charge par un système de messagerie sous-jacent dans un flux binaire pouvant être transféré avec le message lorsqu'un fournisseur de transport l'envoie. Le fournisseur de transport qui reçoit le message peut ensuite décoder le flux binaire pour récupérer toutes les propriétés du message d'origine et les rendre accessibles aux applications clientes. Le modèle opérationnel pour TNEF est le suivant:
  
- Les clients de messagerie envoient et reçoivent des messages vers un transport TNEF comme d'habitude.
    
- Le transport sépare les propriétés des messages sortants en deux catégories: celles que le système de messagerie sous-jacent prend en charge et celles qui ne le sont pas. Les valeurs des propriétés prises en charge par le système de messagerie sous-jacent sont converties dans le format requis.
    
- Le transport utilise les méthodes TNEF MAPI pour coder les propriétés non prises en charge dans un seul flux de données. Le transport transforme alors ce flux de données en pièce jointe spéciale sur le message sortant, en utilisant le modèle de pièce jointe du système de messagerie sous-jacent, avant d'envoyer le message.
    
- Un transport activé TNEF qui reçoit ce type de message effectue deux actions. Tout d'abord, il traduit les propriétés du message entrant, c'est-à-dire celles prises en charge par le système de messagerie sous-jacent, dans les propriétés MAPI. Deuxièmement, si la pièce jointe spéciale est présente, elle utilise les méthodes TNEF MAPI pour récupérer des propriétés MAPI supplémentaires à partir de la pièce jointe avant de remettre le message à une application cliente.
    
MAPI fournit une implémentation de l'interface **ITnef** pour une utilisation par les fournisseurs de transport MAPI lors de l'utilisation d'objets TNEF. La fonction [OpenTnefStreamEx](opentnefstreamex.md) permet de créer des objets TNEF et de les associer à un message. Les flux TNEF sont créés en plus de l'interface OLE **IStream** . 
  
> [!NOTE]
> Vous utilisez **OpenTnefStreamEx** pour créer des objets TNEF. L'ancienne fonction **OpenTnefStream** existe toujours pour des incompatibilités avec le code source ancien et ne doit pas être utilisée dans les nouveautés. 
  
L'interface **ITnef** fournit les méthodes suivantes: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Le modèle d'implémentation MAPI TNEF prend en charge les éléments suivants:
  
- Toutes les propriétés MAPI sans affecter les autres propriétés de message. Pour que les messages MAPI survivent le transport via un système de messagerie, toutes les propriétés qui ne peuvent pas être codées en tant que propriétés du système de messagerie doivent être encapsulées. Étant donné qu'il n'est presque jamais connu lors de l'envoi d'un message qu'un client conforme à la norme MAPI reçoit le message, le schéma d'encapsulation permet à un fournisseur de transport de coder uniquement les propriétés de message MAPI non répertoriées par le système de messagerie. prise en charge native. Cela signifie que les messages qui utilisent TNEF ne sont pas «opaques» pour les systèmes de messagerie qui ne sont pas basés sur MAPI, tels que les systèmes de messagerie UNIX SMTP. Ces systèmes reçoivent les propriétés qu'ils prennent en charge de la manière habituelle pour eux, et d'autres propriétés sont reçues sous la forme d'un flux de données encodé TNEF. Le fournisseur de transport TNEF est chargé de différencier ces deux ensembles de propriétés et d'envoyer le jeu pris en charge de la manière appropriée pour le système de messagerie. Le format TNEF ne fait aucune supposition quant au niveau de prise en charge fourni par un système de messagerie. Toutefois, dans les exemples de l'utilisation de TNEF incluse dans cette section, l'hypothèse est que le système de messagerie prend en charge au moins une seule pièce jointe du message. Dans certains cas, la pièce jointe ne peut être prise en charge que par le biais d'un flux UUEncoded et est transmise dans le texte du message. Le système de messagerie est tellement peu pris en charge pour les propriétés de message que le codage TNEF complet de toutes les propriétés est nécessaire.
    
- Mécanisme permettant de déterminer si un flux TNEF sur un message entrant appartient au message, en fonction de la propriété MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Cette propriété doit être trouvée dans le flux TNEF et dans un en-tête de message approprié. Si la propriété a la même valeur aux deux endroits ou manquante à partir de n'importe quel endroit, le flux TNEF est supposé appartenir au message. Dans le cas contraire, le flux TNEF est ignoré. Les transports activés par TNEF sont chargés de choisir une valeur pour cette propriété sur les messages sortants et de l'encoder dans un en-tête de message approprié (par exemple, l'en-tête Message-ID: pour les messages SMTP) et dans le flux TNEF.
    

