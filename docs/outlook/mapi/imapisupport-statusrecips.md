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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341768"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Génère des rapports de remise et de livraison.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> dans Pointeur vers le message pour lequel le rapport doit être généré.
    
 _lpRecipList_
  
> dans Pointeur vers une structure [ADRLIST](adrlist.md) qui décrit les destinataires du message désigné par _lpMessage_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le rapport a été généré avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L'appel a réussi globalement, mais il n'y a pas d'options de destinataire pour ce type de destinataire. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: StatusRecips** est implémentée pour les objets de prise en charge du fournisseur de transport. Les fournisseurs de transport appellent **StatusRecips** pour demander que MAPI envoie un rapport de remise ou de non-remise à un ensemble d'un ou de plusieurs destinataires d'un message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez appeler **StatusRecips** plusieurs fois pendant le traitement d'un message. Toutefois, si vous appelez **StatusRecips** pour un message ouvert, vous pouvez collecter toutes les informations de remise et de non-remise pour les destinataires du message et appeler **StatusRecips** pour cette liste de destinataires. Un seul point de collection est important, car plusieurs appels **StatusRecips** pour un destinataire peuvent entraîner l'envoi de plusieurs rapports identiques. 
  
Stockez les propriétés liées à la remise ou non à la remise des messages dans la structure **ADRLIST** indiquée par le paramètre _lpRecipList_ . Pour obtenir la liste complète des propriétés requises et facultatives pour les rapports de remise et les rapports de non-remise, voir [Required Report message](required-report-message-properties.md) Properties et [Optional Report Message Properties](optional-report-message-properties.md). 
  
AlLouez de la mémoire pour la structure **ADRLIST** dans _lpRecipList_ à l'aide des fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) . MAPI libère la mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **StatusRecips** réussit. 
  
Pour obtenir une vue d'ensemble des rapports de remise et de non-remise, consultez la rubrique [MAPI Report messages](mapi-report-messages.md).
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

