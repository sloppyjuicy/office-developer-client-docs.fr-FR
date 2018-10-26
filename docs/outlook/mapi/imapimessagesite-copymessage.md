---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 074a806a710ce8c11adba815951c93c25d8cae7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579255"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie le message en cours dans un dossier.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Paramètres

 _pFolderDestination_
  
> [in] Pointeur vers le dossier dans lequel le message doit être copiée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas pris en charge par ce site de message.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIMessageSite::CopyMessage** pour copier le message actuel dans un nouveau dossier. **CopyMessage** ne modifie pas le message affiché à l’utilisateur, et aucun l’interface pour le message nouvellement créé n’est renvoyé à l’écran. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Une implémentation classique de la méthode **CopyMessage** effectue les tâches suivantes : 
  
1. Crée un nouveau message pour le message en cours à copier dans.
    
2. Appelle la méthode [IPersistMessage::Save](ipersistmessage-save.md) avec un pointeur vers le nouveau message dans le paramètre _pMessage_ et FALSE dans le paramètre _fSameAsLoad_ . 
    
3. Appelle la méthode [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , en passant NULL dans le paramètre _pMessage_ . 
    
4. Appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le nouveau message. 
    
Pour obtenir la liste des interfaces qui sont liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

