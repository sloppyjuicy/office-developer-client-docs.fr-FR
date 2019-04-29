---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437650"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Encode une vue pour la table de destinataires d'un message dans le flux de données TNEF (Transport-Neutral Encapsulation Format) du message.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpRecipientTable_
  
> dans Pointeur vers la table de destinataire pour laquelle l'affichage est encodé. Le paramètre _lpRecipientTable_ peut être null. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: EncodeRecips** pour effectuer un codage TNEF pour une vue de table de destinataires particulière. Le codage TNEF est utile, par exemple, si un fournisseur ou une passerelle nécessite un jeu de colonnes, un ordre de tri ou une restriction particulière pour la table des destinataires. 
  
Un fournisseur ou une passerelle passe l'affichage tableau à coder dans le paramètre _lpRecipientTable_ . L'implémentation TNEF encode la table de destinataires avec l'affichage donné à l'aide du jeu de colonnes donné, de l'ordre de tri, de la restriction et de la position. Si un fournisseur ou une passerelle transmet NULL dans _lpRecipientTable_, TNEF obtient la table de destinataires à partir du message en cours de codage à l'aide de la méthode [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) , puis traite chaque ligne de la table dans le flux TNEF à l'aide du paramètres actuels de la table. 
  
L'appel de **EncodeRecips** avec NULL dans _lpRecipientTable_ code tous les destinataires de message et équivaut à l'appel de la méthode [ITnef:: AddProps](itnef-addprops.md) avec l'indicateur TNEF_PROP_INCLUDE dans son paramètre _ulFlags_ et le **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans son paramètre _lpPropList_ . 
  
Notez qu'il est rarement nécessaire d'appeler **EncodeRecips** à moins qu'il ne soit nécessaire de coder une vue de table de destinataires particulière. Les systèmes de messagerie étrangers disposent presque toujours de fonctionnalités permettant de gérer les listes de destinataires suffisamment puissantes pour répondre aux besoins communs d'encodage des listes de destinataires; par conséquent, ces systèmes n'ont presque jamais besoin de format TNEF à cet effet. 
  
## <a name="see-also"></a>Voir aussi



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

