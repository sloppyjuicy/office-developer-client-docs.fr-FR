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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7813636abc1c4d6ad756c7cf670e21d4acb7f540
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592744"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Avertit le formulaire qui un enregistrement opération a été effectuée. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Paramètres

_pMessage_
  
> [in] Pointeur vers le message nouvellement enregistré.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La notification a réussi.
    
E_INVALIDARG 
  
> Le paramètre _pMessage_ est NULL, le formulaire est soit à l’état [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
E_UNEXPECTED 
  
> Le formulaire n’est pas dans un des états suivants :
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Remarques

La méthode **IPersistMessage::SaveCompleted** est appelée par une visionneuse de formulaire pour notifier le formulaire toutes les modifications en attente ont été enregistrées. **Méthode SaveCompleted** doit être appelée uniquement lorsque le formulaire est dans un des états suivants : 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Il existe plusieurs actions possibles que la méthode de la **méthode SaveCompleted** peut effectuer, selon le message le paramètre de pointeur contient et état le message se trouve dans. Toutefois, lorsqu’une action réussit, toujours enregistrer l’état actuel du message vers laquelle pointe le paramètre _pMessage_ et transition du formulaire à son état [Normal](normal-state.md) . 
  
Le tableau suivant décrit les conditions qui affectent les actions à qu'entreprendre dans votre implémentation de la **méthode SaveCompleted**.
  
|**Condition**|**Action**|
|:-----|:-----|
|Le paramètre _pMessage_ est NULL, et le paramètre _fSameAsLoad_ de la méthode [IPersistMessage::Save](ipersistmessage-save.md) est défini sur TRUE.  <br/> |Appelez la méthode [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de tous les utilisateurs inscrits, marquer le formulaire en tant que S_OK clean et de retour.  <br/> |
|Le paramètre _pMessage_ est NULL, et le paramètre _fSameAsLoad_ de la méthode **IPersistMessage::Save** est défini sur FALSE.  <br/> |Elles retournent S_OK.  <br/> |
|Le formulaire est dans l’état HandsOffFromNormal.  <br/> |Libérer le message en cours et remplacez-le par le message vers laquelle pointé le paramètre _pMessage_ . Appelez la méthode [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du message de remplacement et qu’elles retournent S_OK.  <br/> |
|Le formulaire est dans l’état HandsOffAfterSave.  <br/> |Appelez la méthode **IMAPIViewAdviseSink::OnSaved** de tous les utilisateurs inscrits, marquer le formulaire en tant que S_OK clean et de retour.  <br/> |
|Le formulaire est dans l’état [NoScribble](noscribble-state.md) .  <br/> |Libérer le message en cours et remplacez-le par le message vers lequel pointé _pMessage_. Appeler la méthode **IUnknown::AddRef** du message de remplacement. Appelez la méthode **IMAPIViewAdviseSink::OnSaved** de tous les utilisateurs inscrits, marquer le formulaire en tant que S_OK clean et de retour.  <br/> |
|Le formulaire est dans un des États HandsOff et le paramètre _pMessage_ est défini sur NULL.  <br/> |Retour E_INVALIDARG.  <br/> |
|Le formulaire est dans un état autre qu’un des États HandsOff ou l’état NoScribble.  <br/> |Retourner E_UNEXPECTED.  <br/> |
   
Pour plus d’informations sur l’enregistrement des objets de stockage, voir la documentation pour les méthodes [IPersistStorage::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>Voir aussi

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [États de formulaire](form-states.md)
