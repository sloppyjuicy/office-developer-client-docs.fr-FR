---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d7fea09943c1c39275557d1386c0d351be1de82b
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464749"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie le message actuel dans un dossier.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Paramètres

 _pFolderDestination_
  
> [in] Pointeur vers le dossier dans lequel le message doit être copié.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas prise en charge par ce site de message.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIMessageSite::CopyMessage** pour copier le message actuel dans un nouveau dossier. **CopyMessage** ne modifie pas le message actuellement affiché à l’utilisateur et aucune interface du message nouvellement créé n’est renvoyée au formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Une implémentation classique de la **méthode CopyMessage** effectue les tâches suivantes : 
  
1. Crée un message pour le message actuel à copier.
    
2. Appelle la [méthode IPersistMessage::Save](ipersistmessage-save.md) avec un pointeur vers le nouveau message dans le paramètre _pMessage_ et FALSE dans le paramètre _fSameAsLoad_ . 
    
3. Appelle la [méthode IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , en passant NULL dans le _paramètre pMessage_ . 
    
4. Appelle la [méthode IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le nouveau message. 
    
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [INTERFACES DE FORMULAIRE MAPI](mapi-form-interfaces.md).
  
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


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

