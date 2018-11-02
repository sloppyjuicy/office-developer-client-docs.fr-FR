---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cda629cf78d3f7915b64c130867ed4f8ebbd6f8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563841"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Génère des rapports de remise et de non-remise.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message pour lequel le rapport doit être généré.
    
 _lpRecipList_
  
> [in] Un pointeur vers une structure [ADRLIST](adrlist.md) qui décrit les destinataires du message indiqué par _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le rapport a été généré.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais aucune option de destinataire pour ce type de destinataire. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::StatusRecips** est implémentée pour les objets de prise en charge de fournisseur de transport. Fournisseurs de transport appeler **StatusRecips** pour demander qu’envoi MAPI un rapport de remise ou de non-remise à un ensemble d’une ou plusieurs des destinataires d’un message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez appeler **StatusRecips** plusieurs fois lors du traitement d’un message. Toutefois, si vous appelez **StatusRecips** pour un message ouvert, faites votre possible pour toutes les informations de remise et de non-remise pour les destinataires du message et appeler **StatusRecips** pour cette liste de destinataires. Un point unique de la collection est important, car plusieurs appels **StatusRecips** pour un destinataire peuvent générer plusieurs rapports identiques envoyés. 
  
Stocker les propriétés qui sont associées à la remise du message ou de non-remise dans la structure **ADRLIST** indiquée par le paramètre _lpRecipList_ . Pour une liste complète des propriétés obligatoires et facultatifs de rapports de remise et des rapports de non-remise, voir [Propriétés de Message de rapport requises](required-report-message-properties.md) et les [Propriétés de Message de rapport facultatif](optional-report-message-properties.md). 
  
Allouer de la mémoire pour la structure **ADRLIST** dans _lpRecipList_ en utilisant les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) . MAPI libère la mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **StatusRecips** réussit. 
  
Pour une vue d’ensemble des rapports de remise et de non-remise, voir [Les Messages de rapport MAPI](mapi-report-messages.md).
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

