---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
ms.openlocfilehash: 203b3a40469eec264fa3aeff6a0fd5ca3db3f642
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370350"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Paramètres

 _pMessage_
  
> [in] Pointeur vers le message.
    
 _fSameAsLoad_
  
> [in] TRUE pour indiquer que le message pointé par  _pMessage_ est le message à partir duquel le formulaire a été chargé ou créé ; sinon, FALSE. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a été enregistré avec succès.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IPersistMessage::Save** pour enregistrer un formulaire révisé dans le message à partir duquel il a été chargé ou créé. 
  
 **L’enregistrer** ne doit être appelé que lorsque le formulaire est dans son [état Normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ne pas valider les modifications enregistrées ; C’est à l’appelant de valider les modifications. Ne modifiez jamais les propriétés qui appartiennent au message du formulaire, sauf pendant **l’appel d’enregistrer** . 
  
Si  _fSameAsLoad_ est définie sur TRUE, vous pouvez enregistrer les modifications apportées au message existant du formulaire. Si  _fSameAsLoad_ est définie sur FALSE, vous devez copier toutes les propriétés du message d’origine dans le message pointé par  _pMessage_ avant d’effectuer l’enregistrer. Utilisez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés. 
  
Lorsque toutes les propriétés ont été copiées, entrez [l’état NoScribble](noscribble-state.md) . Si aucune erreur ne se produit, renvoyez S_OK. Sinon, renvoyer l’erreur à partir de l’action qui a échoué. 
  
Si **Save** est appelé lorsque le formulaire est dans un état autre que Normal, renvoyer E_UNEXPECTED. 
  
Pour plus d’informations sur l’enregistrement des objets de stockage, voir la documentation sur les méthodes [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[États de formulaire](form-states.md)

