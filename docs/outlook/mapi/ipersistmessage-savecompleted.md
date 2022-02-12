---
title: IPersistMessageSaveCompleted
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9110b86315c9842e3e97d4b220f08d4ca5309aa5
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774866"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit le formulaire qu’une opération d’enregistrer a été effectuée. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Paramètres

_pMessage_
  
> [in] Pointeur vers le message récemment enregistré.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
E_INVALIDARG 
  
> Le  _paramètre pMessage_ est NULL et le formulaire est à l’état [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> Le formulaire n’est pas dans l’un des états suivants :
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Remarques

La **méthode IPersistMessage::SaveCompleted** est appelée par une visionneuse de formulaires pour informer le formulaire que toutes les modifications en attente ont été enregistrées. **SaveCompleted** doit être appelé uniquement lorsque le formulaire se trouve dans l’un des états suivants : 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Il existe plusieurs actions possibles que la méthode **SaveCompleted** peut effectuer, en fonction du contenu du paramètre de pointeur de message et de l’état dans le message. Toutefois, lorsqu’une action réussit, enregistrez toujours l’état actuel du message vers qui pointe le paramètre  _pMessage_ et transition du formulaire à son [état](normal-state.md) Normal. 
  
Le tableau suivant décrit les conditions qui affectent les actions que vous devez prendre dans votre implémentation de **SaveCompleted**.
  
|**Condition**|**Action**|
|:-----|:-----|
|Le  _paramètre pMessage_ est NULL et le paramètre  _fSameAsLoad_ de la méthode [IPersistMessage::Save](ipersistmessage-save.md) est définie sur TRUE. |Appelez [la méthode IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de toutes les visionneuses inscrites, marquez le formulaire comme propre et renvoyez S_OK. |
|Le  _paramètre pMessage_ est NULL et le paramètre  _fSameAsLoad_ de la méthode **IPersistMessage::Save** est définie sur FALSE. |Elles retournent S_OK. |
|Le formulaire est à l’état HandsOffFromNormal. |Relâchez le message actuel et remplacez-le par le message pointé par  _le paramètre pMessage_ . Appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du message de remplacement et renvoyez S_OK. |
|Le formulaire est à l’état HandsOffAfterSave. |Appelez **la méthode IMAPIViewAdviseSink::OnSaved** de toutes les visionneuses inscrites, marquez le formulaire comme propre et renvoyez S_OK. |
|Le formulaire est dans [l’état NoScribble](noscribble-state.md) . |Relâchez le message actuel et remplacez-le par le message pointé  _par pMessage_. Appelez la méthode **IUnknown::AddRef** du message de remplacement. Appelez **la méthode IMAPIViewAdviseSink::OnSaved** de toutes les visionneuses inscrites, marquez le formulaire comme propre et renvoyez S_OK. |
|Le formulaire est dans l’un des états HandsOff et le  _paramètre pMessage_ est définie sur NULL. |Renvoyer E_INVALIDARG. |
|Le formulaire est dans un état autre que l’un des états HandsOff ou NoScribble. |Renvoyer E_UNEXPECTED. |
   
Pour plus d’informations sur l’enregistrement des objets de stockage, voir la documentation des méthodes [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Voir aussi

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [États de formulaire](form-states.md)
