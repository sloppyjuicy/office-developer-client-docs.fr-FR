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
ms.openlocfilehash: 839eef63a93510df6f5ea854ed2e2e678e7823d3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377805"
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) représentant l’interface à utiliser pour accéder au message. La transmission DE NULL entraîne le retour de l’interface standard du message, **ou IMessage**. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la pièce jointe est créée. L’indicateur suivant peut être définie :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **CreateAttach de** renvoyer correctement, éventuellement avant que la pièce jointe soit entièrement accessible au client appelant. Si la pièce jointe n’est pas accessible, un appel ultérieur peut entraîner une erreur. 
    
 _lpulAttachmentNum_
  
> [out] Pointeur vers un numéro d’index identifiant la pièce jointe nouvellement créée. Ce numéro n’est valide que lorsque le message est ouvert et constitue la base de la propriété **PR_ATTACH_NUM (**[PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.
    
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

