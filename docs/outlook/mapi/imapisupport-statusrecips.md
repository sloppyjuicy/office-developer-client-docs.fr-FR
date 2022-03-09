---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
ms.openlocfilehash: a70dcf429501af176fc0927f047b9d8fb6d07db1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370826"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Génère des rapports de remise et de non remise.
  
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
  
> [in] Pointeur vers une structure [ADRLIST](adrlist.md) qui décrit les destinataires du message pointés par  _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le rapport a été généré avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi globalement, mais il n’existe aucune option de destinataire pour ce type de destinataire. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED’avertissement** . Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::StatusRecips est** implémentée pour les objets de prise en charge du fournisseur de transport. Les fournisseurs de transport **appellent StatusRecips** pour demander à MAPI d’envoyer un rapport de remise ou de non remise à un ensemble d’un ou plusieurs destinataires d’un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler **StatusRecips plusieurs** fois pendant le traitement d’un message. Toutefois, si vous appelez **StatusRecips** pour un message ouvert, faites de votre mieux pour collecter toutes les informations de remise et de remise pour les destinataires du message et appeler **StatusRecips** pour cette liste de destinataires. Un point de collecte unique est important, car plusieurs appels **StatusRecips** pour un destinataire peuvent entraîner l’envoi de plusieurs rapports identiques. 
  
Stockez les propriétés liées à la remise ou à la non remise des messages dans la structure **ADRLIST** indiquée par  _le paramètre lpRecipList_ . Pour obtenir la liste complète des propriétés requises et facultatives pour les rapports de remise et les rapports non remise, voir [Propriétés de message](required-report-message-properties.md) de rapport requises et [propriétés facultatives du message de rapport](optional-report-message-properties.md). 
  
Allouez de la mémoire pour la structure **ADRLIST** dans  _lpRecipList_ à l’aide des fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) . MAPI libère la mémoire en appelant la [fonction MAPIFreeBuffer](mapifreebuffer.md) uniquement si **StatusRecips** réussit. 
  
Pour une vue d’ensemble des rapports de remise et de non remise, voir [MESSAGES de rapport MAPI](mapi-report-messages.md).
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

