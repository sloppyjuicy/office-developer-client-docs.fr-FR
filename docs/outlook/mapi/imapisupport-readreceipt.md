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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784046"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**S’applique à**: Outlook 
  
Génère un rapport nonread pour un message ou en lecture.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la lecture ou l’état nonread est généré. Vous pouvez définir l’indicateur suivant :
    
MAPI_NON_READ 
  
> Un rapport nonread est généré. Si MAPI_NON_READ n’est pas définie, un rapport de lecture est généré.
    
 _lpReadMessage_
  
> [in] Pointeur vers le message sur lequel le rapport doit être généré.
    
 _lppEmptyMessage_
  
> [entrée, sortie] À l’entrée _lppEmptyMessage_ pointe vers un pointeur vers un message vide. Dans la sortie, _lppEmptyMessage_ pointe vers un pointeur vers le message d’état. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le rapport a été généré.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::ReadReceipt** est implémentée uniquement pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de magasins message appellent **ReadReceipt** pour indiquer à MAPI pour générer un rapport nonread pour le message vers laquelle pointé le paramètre _lpReadMessage_ ou en lecture. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appel **ReadReceipt** lorsque la valeur de la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et une des conditions suivantes est vraie :
  
- Le message a été lu.
    
- Le message a été déplacé.
    
- Le message a été copié.
    
- Méthode de [IMessage::SetReadFlag](imessage-setreadflag.md) du message a été appelée. 
    
N’appelez pas **ReadReceipt** lorsqu’un message est supprimé. 
  
Un rapport nonread ou en lecture doit être envoyé qu’une seule fois pour un message. Garder une trace des état de lecture d’un message et ne pas envoyer de rapports multiples pour un seul message.
  
Si le paramètre _lppEmptyMessage_ pointe vers un message de rapport valide MAPI retourne à partir de **ReadReceipt**, appelez la méthode de [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message et puis relâchez le pointeur en appelant son **IUnknown:s:Release **méthode. 
  
Si **ReadReceipt** échoue, le message doit être libéré sans soumis. Si vous stockez état de lecture du message, vous pouvez tenter de générer le lire ou nonread à une date ultérieure. 
  
Vous pouvez masquer ou afficher des rapports de lecture et nonread générés par magasins dans vos dossiers. Stockage des rapports de lecture et nonread dans des dossiers cachés vous permet d’implémenter une sécurité accrue.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propriété canonique PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

