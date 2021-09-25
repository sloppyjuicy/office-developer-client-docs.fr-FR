---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1d334a273f0f454c59ea2c28b98e4e5bac6b809d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556622"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le message actuel.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Paramètres

 _ppmsg_
  
> [out] Pointeur vers un pointeur vers l’interface renvoyée pour le message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
S_FALSE 
  
> Il n’existe actuellement aucun message pour le formulaire appelant.
    
## <a name="remarks"></a>Remarques

Les formulaires appellent la méthode **IMAPIMessageSite::GetMessage** pour obtenir une interface de message pour le message actuel. Le message actuel est le même message que celui qui a été passé précédemment dans la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)ou [IPersistMessage::SaveCompleted.](ipersistmessage-savecompleted.md) 
  
 **GetMessage** renvoie S_FALSE si aucun message n’existe actuellement. Cet état peut se produire après les appels à la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) ou avant l’appel suivant à **IPersistMessage::Load** ou **IPersistMessage::SaveCompleted** est effectué. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetMessage** pour renvoyer le pointeur de message actuellement mis en cache, s’il est disponible.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

