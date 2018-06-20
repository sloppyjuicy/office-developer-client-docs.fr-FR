---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784359"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**S’applique à**: Outlook 
  
Enregistre un formulaire révisé dans le message à partir de laquelle il a été chargé ou créé.
  
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
  
> [in] TRUE pour indiquer que le message vers lequel pointe par _pMessage_ est le message à partir de laquelle le formulaire a été chargé ou créé ; Sinon, FALSE. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le formulaire a été enregistré avec succès.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IPersistMessage::Save** pour enregistrer un formulaire révisé dans le message à partir de laquelle il a été chargé ou créé. 
  
 **Enregistrer** doit être appelée uniquement lorsque le formulaire est dans son état [Normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Ne vous engagez pas les modifications enregistrées ; C’est à l’appelant pour valider les modifications. Ne jamais modifier les propriétés qui appartiennent au message du formulaire à l’exception lors de l’appel à **Enregistrer** . 
  
Si _fSameAsLoad_ est défini sur TRUE, vous pouvez enregistrer les modifications apportées à un message existant du formulaire. Si _fSameAsLoad_ est défini sur FALSE, vous devez copier toutes les propriétés à partir du message d’origine dans le message vers lequel pointé _pMessage_ avant d’effectuer l’enregistrement. Utilisez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés. 
  
Lorsque toutes les propriétés ont été copiés, entrez l’état [NoScribble](noscribble-state.md) . Si aucune erreur ne se produire, retournent S_OK. Sinon, renvoie l’erreur de l’action a échoué. 
  
Si vous **enregistrez** est appelée lorsque le formulaire est dans un état autre que Normal, retourner E_UNEXPECTED. 
  
Pour plus d’informations sur l’enregistrement des objets de stockage, consultez la documentation sur les méthodes [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[États de formulaire](form-states.md)

