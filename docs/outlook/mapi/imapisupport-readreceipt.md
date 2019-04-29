---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425322"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Génère un rapport de lecture ou de non-lecture pour un message.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le rapport de lecture ou de non-lecture est généré. L'indicateur suivant peut être défini:
    
MAPI_NON_READ 
  
> Un rapport non lu est généré. Si MAPI_NON_READ n'est pas défini, un rapport de lecture est généré.
    
 _lpReadMessage_
  
> dans Pointeur vers le message à propos duquel le rapport doit être généré.
    
 _lppEmptyMessage_
  
> [in, out] Lors de l'entrée, _lppEmptyMessage_ pointe vers un pointeur vers un message vide. En sortie, _lppEmptyMessage_ pointe vers un pointeur vers le message de rapport. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le rapport a été généré avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: ReadReceipt** est implémentée uniquement pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages appellent **ReadReceipt** pour indiquer à MAPI de générer un rapport de lecture ou de non-lecture pour le message pointé par le paramètre _lpReadMessage_ . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **ReadReceipt** lorsque la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie et que l'une des conditions suivantes est vraie:
  
- Le message a été lu.
    
- Le message a été déplacé.
    
- Le message a été copié.
    
- La méthode [IMessage:: SetReadFlag](imessage-setreadflag.md) du message a été appelée. 
    
N'appelez pas **ReadReceipt** lorsqu'un message est supprimé. 
  
Un rapport de lecture ou de non-lecture ne doit être envoyé qu'une seule fois pour un message. Assurer le suivi de l'état de lecture d'un message et ne pas envoyer plusieurs rapports pour un seul message.
  
Si le paramètre _lppEmptyMessage_ pointe vers un message de rapport valide lorsque MAPI revient de **ReadReceipt**, appelez la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) pour envoyer le message, puis libérez le pointeur en appelant sa propriété **IUnknown: s: Release. **méthode. 
  
Si **ReadReceipt** échoue, le message doit être libéré sans être soumis. Si vous stockez l'état de lecture du message, vous pouvez essayer de générer le rapport de lecture ou de non-lecture ultérieurement. 
  
Vous pouvez masquer ou afficher les rapports lus et non lus générés par les banques dans vos dossiers. Le stockage des rapports lus et non lus dans des dossiers cachés vous permet d'implémenter une sécurité plus étroite.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propriété canonique PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

