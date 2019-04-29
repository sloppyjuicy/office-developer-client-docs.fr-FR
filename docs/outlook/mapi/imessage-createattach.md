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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417670"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une nouvelle pièce jointe.
  
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
  
> dans Pointeur vers l'identificateur d'interface (IID) représentant l'interface à utiliser pour accéder au message. Le fait de transmettre des résultats NULL dans l'interface standard du message, ou **IMessage**, est retourné. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont la pièce jointe est créée. L'indicateur suivant peut être défini:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **CreateAttach** de renvoyer correctement, éventuellement avant que la pièce jointe soit totalement accessible au client appelant. Si la pièce jointe n'est pas accessible, un appel ultérieur de celle-ci peut entraîner une erreur. 
    
 _lpulAttachmentNum_
  
> remarquer Pointeur vers un numéro d'index identifiant la pièce jointe nouvellement créée. Ce nombre est valide uniquement lorsque le message est ouvert et constitue la base de la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.
    
 _lppAttach_
  
> remarquer Pointeur vers un pointeur vers l'objet Attachment ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La pièce jointe a été créée.
    
## <a name="remarks"></a>Remarques

La méthode **IMessage:: CreateAttach** crée une nouvelle pièce jointe dans un message. La nouvelle pièce jointe et toutes les propriétés qui y sont définies ne sont pas disponibles tant qu'un client n'a pas appelé la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la pièce jointe et la méthode **IMAPIProp:: SaveChanges** du message. 
  
Le numéro de pièce jointe désigné par _lpulAttachmentNum_ est unique et valide uniquement dans le contexte du message. Autrement dit, deux pièces jointes dans deux messages différents peuvent avoir le même nombre tandis que deux pièces jointes dans le même message ne le peuvent pas. 
  
## <a name="see-also"></a>Voir aussi



[IMessage : IMAPIProp](imessageimapiprop.md)

