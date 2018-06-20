---
title: Développement d’un fournisseur de Transport prenant en charge TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9f80feecda219e3bcebbf8ceb346b5034e821470
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783161"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Développement d’un fournisseur de Transport prenant en charge TNEF

  
  
**S’applique à**: Outlook 
  
Pour promouvoir l’interopérabilité entre les systèmes de messagerie qui prennent en charge différentes fonctionnalités MAPI, MAPI fournit le Transport Neutral Encapsulation Format TNEF () en tant que standard permet de transférer des données. Ce format encapsule des propriétés MAPI non pris en charge par un système de messagerie sous-jacent dans un objet stream binaire qui peut être transféré ainsi que le message lorsque envoie un fournisseur de transport. Le fournisseur de transport qui reçoit le message peut décoder puis le flux binaire pour récupérer toutes les propriétés du message d’origine et les rendre disponibles pour les applications clientes. Le modèle opérationnel pour TNEF est la suivante :
  
- Clients de messagerie envoyant et recevoir des messages à un transport TNEF comme d’habitude.
    
- Le transport sépare les propriétés sur les messages sortants en deux catégories : celles prenant en charge le système de messagerie sous-jacent et il n’existe pas. Les valeurs des propriétés qui sont prises en charge par le système de messagerie sous-jacent sont converties dans le format requis.
    
- Le transport utilise les méthodes de MAPI TNEF pour coder toutes les propriétés non prises en charge dans un flux de données. Le transport puis transforme ce flux de données particulière d’une pièce jointe dans le message sortant, à l’aide du modèle de pièce jointe du système de messagerie sous-jacent, avant d’envoyer le message.
    
- Un type de transport TNEF activé qui reçoit un message de ce type exécute deux tâches. Tout d’abord, traduit les propriétés du message entrant — ceux pris en charge par le système de messagerie sous-jacent, dans propriétés MAPI. Deuxièmement, si la pièce jointe spéciale n’est présente, il utilise les méthodes de MAPI TNEF pour récupérer les propriétés MAPI supplémentaires à partir de la pièce jointe avant de remettre le message à une application cliente.
    
MAPI fournit une implémentation de l’interface **ITnef** pour une utilisation par des fournisseurs de transport MAPI lorsque vous travaillez avec des objets TNEF. La fonction [OpenTnefStreamEx](opentnefstreamex.md) est utilisée pour créer des objets TNEF et les associer à un message. Flux TNEF sont basées sur l’interface OLE **IStream** 
  
> [!NOTE]
> **OpenTnefStreamEx** vous permet de créer des objets TNEF. La fonction **OpenTnefStream** ancienne toujours pour assurer la compatibilité avec l’ancien code source et ne doit pas être utilisée dans un nouveau. 
  
L’interface **ITnef** fournit les méthodes suivantes : 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Terminer](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Le modèle de mise en œuvre MAPI TNEF prend en charge :
  
- Toutes les propriétés MAPI sans affecter d’autres propriétés de message. Dans l’ordre pour les messages de survivre transport via un système de messagerie MAPI, toutes les propriétés qui ne peuvent pas être codées en tant que propriétés du système de messagerie doivent être encapsulées. Car il est presque jamais connu au moment où qu'un message est envoyé ou non un client compatible MAPI le message, le jeu d’encapsulation permet à un fournisseur de transport à coder uniquement les propriétés de message MAPI qui n’est pas le cas du système de messagerie prend en charge. Cela signifie que les messages qui utilisent le format TNEF ne sont pas « opaques » pour les systèmes de messagerie qui ne reposent sur MAPI, tel que UNIX basé sur SMTP systèmes de messagerie. Ces systèmes reçoivent les propriétés qu’ils prennent en charge de quelque manière par défaut pour les propriétés et d’autres sont reçues en tant qu’un flux de données codé TNEF. Le fournisseur de transport TNEF est chargé de différenciation entre ces deux jeux de propriétés et de l’envoi de l’ensemble de prise en charge de façon appropriée pour le système de messagerie. TNEF n’émet aucune hypothèse que le niveau de prise en charge offerte par un système de messagerie. Toutefois, dans les exemples d’utilisation du format TNEF inclus dans cette section, l’hypothèse est faite que le système de messagerie prend en charge au moins une seule pièce jointe en plus du message. Dans certains cas, la pièce jointe peut uniquement être pris en charge via un flux UUENCODE et transmise dans le cadre du texte du message. Uniquement dans les cas rares le système de messagerie a peu prise en charge pour les propriétés de message ce codage TNEF complète de toutes les propriétés est nécessaire.
    
- Un mécanisme permettant de déterminer si un flux TNEF sur un message entrant appartient au message, selon la propriété MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Cette propriété doit se trouver dans le flux TNEF et dans un en-tête de message approprié. Si la propriété possède la même valeur aux deux endroits, ou est manquante à cet emplacement, le flux TNEF est supposé appartenant au message. Dans le cas contraire, le flux TNEF est ignoré. Transports TNEF activé sont chargés de choix d’une valeur de cette propriété sur les messages sortants et le codage dans un en-tête de message approprié (par exemple, l’ID de Message : en-tête pour les messages SMTP) et dans le flux TNEF.
    

