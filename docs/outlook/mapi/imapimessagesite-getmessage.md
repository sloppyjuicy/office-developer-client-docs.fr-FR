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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3612c12a503174484d4a469ffa167922a015ed5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576609"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie le message en cours.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Paramètres

 _ppmsg_
  
> [out] Pointeur vers un pointeur vers l’interface retournée pour le message.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
S_FALSE 
  
> Aucun message n’existe actuellement pour le formulaire d’appel.
    
## <a name="remarks"></a>Remarques

Formulaires appeler la méthode **IMAPIMessageSite::GetMessage** pour obtenir une interface de message pour le message en cours. Le message en cours est le même message, comme la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)ou [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) a été passé précédemment. 
  
 **GetMessage** renvoie S_FALSE si aucun message n’existe actuellement. Cet état peut se produire après des appels à la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) ou avant l’appel suivant à **IPersistMessage::Load** ou **IPersistMessage::SaveCompleted** est établie. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
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
  
[Interfaces de formulaires MAPI](mapi-form-interfaces.md)

