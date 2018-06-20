---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6351be353100649e38a14543a44df5e115c9408b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784144"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**S’applique à**: Outlook 
  
Crée une pièce jointe.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message. Passant NULL entraîne une interface standard du message ou **IMessage**, renvoyée. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la création de la pièce jointe. Vous pouvez définir l’indicateur suivant :
    
MAPI_DEFERRED_ERRORS 
  
> Permet de **CreateAttach** renvoyer avec succès, éventuellement avant la pièce jointe est accessible au client appelant. Si la pièce jointe n’est pas accessible, passer un appel suivant pour qu’il peut provoquer une erreur. 
    
 _lpulAttachmentNum_
  
> [out] Pointeur vers un numéro d’index qui identifie la pièce jointe nouvellement créée. Ce numéro est valide uniquement lorsque le message est ouvert et la base de la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.
    
 _lppAttach_
  
> [out] Pointeur vers un pointeur vers l’objet d’ouvrir une pièce jointe.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La pièce jointe a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage::CreateAttach** crée une pièce jointe d’un message. La nouvelle pièce jointe et les propriétés qui sont définies, ne sont pas disponibles tant qu’un client a appelé méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la pièce jointe et de méthode de **IMAPIProp::SaveChanges** du message. 
  
Le nombre de pièces jointes désigné par _lpulAttachmentNum_ est unique et valide uniquement dans le contexte du message. Autrement dit, deux pièces jointes dans deux messages différents peuvent avoir le même nombre mais pas les deux pièces jointes dans le même message. 
  
## <a name="see-also"></a>Voir aussi



[IMessage : IMAPIProp](imessageimapiprop.md)

