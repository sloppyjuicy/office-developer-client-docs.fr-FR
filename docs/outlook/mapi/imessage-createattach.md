---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 22735e5d165fb61043bb6433ba84567bf1b3f957
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567360"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) représentant l’interface à utiliser pour accéder au message. La transmission de null entraîne le retour de l’interface standard du message, **ou IMessage.** 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la pièce jointe est créée. L’indicateur suivant peut être définie :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **CreateAttach de** renvoyer correctement, éventuellement avant que la pièce jointe soit entièrement accessible au client appelant. Si la pièce jointe n’est pas accessible, un appel ultérieur peut entraîner une erreur. 
    
 _lpulAttachmentNum_
  
> [out] Pointeur vers un numéro d’index identifiant la pièce jointe nouvellement créée. Ce numéro n’est valide que lorsque le message est ouvert et constitue la base de la propriété PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
    
 _lppAttach_
  
> [out] Pointeur vers un pointeur vers l’objet pièce jointe ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La pièce jointe a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMessage::CreateAttach** crée une pièce jointe sur un message. La nouvelle pièce jointe et les propriétés qui lui sont définies ne sont pas disponibles tant qu’un client n’a pas appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la pièce jointe et la méthode **IMAPIProp::SaveChanges** du message. 
  
Le numéro de pièce jointe pointé par  _lpulAttachmentNum_ est unique et valide uniquement dans le contexte du message. Autrement dit, deux pièces jointes dans deux messages différents peuvent avoir le même nombre, alors que deux pièces jointes dans le même message ne le peuvent pas. 
  
## <a name="see-also"></a>Voir aussi



[IMessage : IMAPIProp](imessageimapiprop.md)

