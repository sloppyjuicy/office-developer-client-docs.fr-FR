---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 39b3ee4328d63c45a822520a999ef2e429acecaf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592234"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Encode une vue de la table des destinataires d’un message dans le flux de données Transport-Neutral Encapsulation Format (TNEF) du message.
  
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
  
> [in] Pointeur vers la table des destinataires pour laquelle l’affichage est codé. Le  _paramètre lpRecipientTable_ peut être NULL. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::EncodeRecips** pour effectuer le codage TNEF pour un affichage de table de destinataires particulier. Le codage TNEF est utile, par exemple, si un fournisseur ou une passerelle requiert un ensemble de colonnes, un ordre de tri ou une restriction particuliers pour la table des destinataires. 
  
Un fournisseur ou une passerelle transmet la vue de table à coder dans le paramètre _lpRecipientTable._ L’implémentation TNEF code la table des destinataires avec l’affichage donné, à l’aide du jeu de colonnes donné, de l’ordre de tri, de la restriction et de la position. Si un fournisseur ou une passerelle transmet la valeur NULL dans  _lpRecipientTable_, le TNEF obtient la table des destinataires à partir du message encodé à l’aide de la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) et traite chaque ligne de la table dans le flux TNEF à l’aide des paramètres actuels de la table. 
  
L’appel de **EncodeRecips** avec NULL dans _lpRecipientTable_ code donc tous les destinataires du message et équivaut à appeler la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE dans son paramètre _ulFlags_ et la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans son paramètre _lpPropList._ 
  
Notez qu’il est rarement nécessaire d’appeler **EncodeRecips,** sauf s’il est nécessaire d’encoder un affichage de table de destinataires particulier. Les systèmes de messagerie étrangers ont presque toujours des installations pour la gestion des listes de destinataires qui sont suffisamment puissantes pour gérer les besoins courants de codage des listes de destinataires ; Par conséquent, ces systèmes ne nécessitent presque jamais le TNEF à cet effet. 
  
## <a name="see-also"></a>Voir aussi



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propriété canonique PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

