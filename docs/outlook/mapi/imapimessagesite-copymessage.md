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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321545"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie le message actif dans un dossier.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Paramètres

 _pFolderDestination_
  
> dans Pointeur vers le dossier dans lequel le message doit être copié.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L'opération n'est pas prise en charge par ce site de messages.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIMessageSite:: CopyMessage** pour copier le message actif dans un nouveau dossier. **CopyMessage** ne change pas le message actuellement affiché à l'utilisateur, et aucune interface n'est renvoyée au formulaire pour le message nouvellement créé. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Une implémentation type de la méthode **CopyMessage** effectue les tâches suivantes: 
  
1. Crée un nouveau message pour le message en cours à copier.
    
2. Appelle la méthode [IPersistMessage:: Save](ipersistmessage-save.md) avec un pointeur vers le nouveau message dans le paramètre _pMessage_ et false dans le paramètre _fSameAsLoad_ . 
    
3. Appelle la méthode [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) , en transmettant la valeur null dans le paramètre _pMessage_ . 
    
4. Appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur le nouveau message. 
    
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: CopyMessage  <br/> |Non implémenté.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

