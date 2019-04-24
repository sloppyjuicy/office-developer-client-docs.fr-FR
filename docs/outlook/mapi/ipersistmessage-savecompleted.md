---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317135"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit le formulaire qu'une opération d'enregistrement a été effectuée. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Paramètres

_pMessage_
  
> dans Pointeur vers le message nouvellement enregistré.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
E_INVALIDARG 
  
> Le paramètre _pMessage_ est null et le formulaire est dans l'état [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> Le formulaire n'est pas dans l'un des États suivants:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Remarques

La méthode **IPersistMessage:: SaveCompleted** est appelée par une visionneuse de formulaires pour informer le formulaire que toutes les modifications en attente ont été enregistrées. **SaveCompleted** doit être appelé uniquement lorsque le formulaire est dans l'un des États suivants: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

La méthode **SaveCompleted** peut effectuer plusieurs actions en fonction de ce que contient le paramètre pointeur de message et de l'État dans lequel se trouve le message. Toutefois, lorsqu'une action réussit, toujours enregistrer l'état actuel du message vers lequel pointe le paramètre _pMessage_ et le faire passer à son état [normal](normal-state.md) . 
  
Le tableau suivant décrit les conditions qui affectent les actions que vous devez suivre lors de l'implémentation de **SaveCompleted**.
  
|**Condition**|**Action**|
|:-----|:-----|
|Le paramètre _pMessage_ est null et le paramètre _fSameAsLoad_ de la méthode [IPersistMessage:: Save](ipersistmessage-save.md) est défini sur true.  <br/> |Appelez la méthode [IMAPIViewAdviseSink:: OnSaved](imapiviewadvisesink-onsaved.md) de toutes les visionneuses inscrites, marquez le formulaire comme Clean et renvoyez S_OK.  <br/> |
|Le paramètre _pMessage_ est null et le paramètre _fSameAsLoad_ de la méthode **IPersistMessage:: Save** est défini sur false.  <br/> |Elles retournent S_OK.  <br/> |
|Le formulaire est dans l'État HandsOffFromNormal.  <br/> |ReLâchez le message en cours et remplacez-le par le message désigné par le paramètre _pMessage_ . Appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du message et retournez S_OK.  <br/> |
|Le formulaire est dans l'État HandsOffAfterSave.  <br/> |Appelez la méthode **IMAPIViewAdviseSink:: OnSaved** de toutes les visionneuses inscrites, marquez le formulaire comme Clean et renvoyez S_OK.  <br/> |
|Le formulaire est dans l' [](noscribble-state.md) État noscribble.  <br/> |ReLâchez le message actif et remplacez-le par le message désigné par _pMessage_. Appelez la méthode **IUnknown:: AddRef** du message. Appelez la méthode **IMAPIViewAdviseSink:: OnSaved** de toutes les visionneuses inscrites, marquez le formulaire comme Clean et renvoyez S_OK.  <br/> |
|Le formulaire se trouve dans l'un des États HandsOff et le paramètre _pMessage_ est défini sur null.  <br/> |Renvoie E_INVALIDARG.  <br/> |
|Le formulaire est dans un État autre que l'un des États HandsOff ou l'État noScribble.  <br/> |Renvoie E_UNEXPECTED.  <br/> |
   
Pour plus d'informations sur l'enregistrement d'objets de stockage, voir la documentation pour les méthodes [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Voir aussi

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [États de formulaire](form-states.md)
