---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321279"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le message actif.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Paramètres

 _ppmsg_
  
> remarquer Pointeur vers un pointeur vers l'interface renvoyée pour le message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
S_FALSE 
  
> Il n'existe actuellement aucun message pour le formulaire appelant.
    
## <a name="remarks"></a>Remarques

Les formulaires appellent la méthode **IMAPIMessageSite:: GetMessage** pour obtenir une interface de message pour le message en cours. Le message actif est le même message que celui précédemment transmis dans la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md), [IPersistMessage:: Load](ipersistmessage-load.md), ou [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) . 
  
 **GetMessage** renvoie S_FALSE si aucun message n'existe actuellement. Cet État peut se produire après les appels à la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) ou avant l'appel suivant à **IPersistMessage:: Load** ou **IPersistMessage:: SaveCompleted** est effectué. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetSession  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite:: GetMessage** pour renvoyer le pointeur de message actuellement mis en cache, s'il est disponible.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

