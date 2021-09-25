---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bd008c7233b191c3e187f6cc44767a9b136a2df8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625405"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Génère un rapport en lecture ou non lu pour un message.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le rapport en lecture ou non lu est généré. L’indicateur suivant peut être définie :
    
MAPI_NON_READ 
  
> Un rapport non lu est généré. Si MAPI_NON_READ n’est pas définie, un rapport de lecture est généré.
    
 _lpReadMessage_
  
> [in] Pointeur vers le message à propos duquel le rapport doit être généré.
    
 _lppEmptyMessage_
  
> [in, out] Lors de  _l’entrée, lppEmptyMessage_ pointe vers un pointeur vers un message vide. En sortie,  _lppEmptyMessage_ pointe vers un pointeur vers le message de rapport. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le rapport a été généré avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::ReadReceipt** est implémentée uniquement pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages appellent **ReadReceipt** pour demander à MAPI de générer un rapport lu ou non lu pour le message pointé par le paramètre _lpReadMessage._ 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **ReadReceipt** lorsque la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie et que l’une des conditions suivantes est vraie :
  
- Le message a été lu.
    
- Le message a été déplacé.
    
- Le message a été copié.
    
- La méthode [IMessage::SetReadFlag](imessage-setreadflag.md) du message a été appelée. 
    
N’appelez **pas ReadReceipt** lorsqu’un message est supprimé. 
  
Un rapport lu ou non lu ne doit être envoyé qu’une seule fois pour un message. Suivez l’état de lecture d’un message et n’envoyez pas plusieurs rapports pour un seul message.
  
Si le paramètre _lppEmptyMessage_ pointe vers un message de rapport valide lorsque MAPI revient de **ReadReceipt,** appelez la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message, puis relâchez le pointeur en appelant sa méthode **IUnknown:s:Release.** 
  
En **cas d’échec de ReadReceipt,** le message doit être libéré sans être envoyé. Si vous stockez l’état de lecture du message, vous pouvez tenter de générer le rapport en lecture ou non lu ultérieurement. 
  
Vous pouvez masquer ou afficher des rapports de lecture et non lus générés par les magasins dans vos dossiers. Le stockage de rapports lus et non lus dans des dossiers masqués vous permet d’implémenter une sécurité plus étroite.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propriété canonique PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

