---
title: IPersistMessageSaveCompleted
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IPersistMessage SaveCompleted, qui avertit le formulaire qu’une opération d’enregistrement a été effectuée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
ms.openlocfilehash: 6885384bd338e4a2a52b839ca82ded3a70c7afed
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828023"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Notifie le formulaire qu’une opération d’enregistrement a été effectuée. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Paramètres

_pMessage_
  
> [in] Pointeur vers le message nouvellement enregistré.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
E_INVALIDARG 
  
> Le paramètre  _pMessage_ est NULL et le formulaire est dans l’état [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> Le formulaire n’est pas dans l’un des états suivants :
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Remarques

La méthode **IPersistMessage::SaveCompleted** est appelée par une visionneuse de formulaires pour informer le formulaire que toutes les modifications en attente ont été enregistrées. **SaveCompleted** doit être appelé uniquement lorsque le formulaire se trouve dans l’un des états suivants : 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Il existe plusieurs actions possibles que la méthode **SaveCompleted** peut effectuer, en fonction de ce que contient le paramètre de pointeur de message et de l’état dans lequel se trouve le message. Toutefois, lorsqu’une action réussit, enregistrez toujours l’état actuel du message vers lequel le paramètre  _pMessage_ pointe et faites passer le formulaire à son état [Normal](normal-state.md) . 
  
Le tableau suivant décrit les conditions qui affectent les actions que vous devez effectuer dans votre implémentation de **SaveCompleted**.
  
|**Condition**|**Action**|
|:-----|:-----|
|Le paramètre  _pMessage_ est NULL et le paramètre  _fSameAsLoad_ de la méthode [IPersistMessage::Save](ipersistmessage-save.md) a la valeur TRUE. |Appelez la méthode [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de tous les visionneuses inscrites, marquez le formulaire comme propre et retournez S_OK. |
|Le paramètre  _pMessage_ est NULL et le paramètre  _fSameAsLoad_ de la méthode **IPersistMessage::Save** a la valeur FALSE. |Elles retournent S_OK. |
|Le formulaire est dans l’état HandsOffFromNormal. |Libérez le message actuel et remplacez-le par le message pointé par le paramètre  _pMessage_ . Appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du message de remplacement et retournez S_OK. |
|Le formulaire est dans l’état HandsOffAfterSave. |Appelez la méthode **IMAPIViewAdviseSink::OnSaved** de tous les visionneuses inscrites, marquez le formulaire comme propre et retournez S_OK. |
|Le formulaire est dans l’état [NoScribble](noscribble-state.md) . |Libérez le message actuel et remplacez-le par le message pointé par  _pMessage_. Appelez la méthode **IUnknown::AddRef** du message de remplacement. Appelez la méthode **IMAPIViewAdviseSink::OnSaved** de tous les visionneuses inscrites, marquez le formulaire comme propre et retournez S_OK. |
|Le formulaire se trouve dans l’un des états HandsOff et le paramètre  _pMessage_ a la valeur NULL. |Retournez E_INVALIDARG. |
|Le formulaire est dans un état autre que l’un des états HandsOff ou l’état NoScribble. |Retournez E_UNEXPECTED. |
   
Pour plus d’informations sur l’enregistrement des objets de stockage, consultez la documentation relative aux méthodes [IPersistStorage::SaveCompleted](/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile::SaveCompleted](/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Voir aussi

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [États de formulaire](form-states.md)
