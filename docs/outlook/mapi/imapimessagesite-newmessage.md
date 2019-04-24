---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321454"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un message.
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Paramètres

 _fComposeInFolder_
  
> dans Indique dans quel dossier le message doit être composé. Si la variable a la valeur FALSe, le paramètre _pFolderFocus_ est ignoré et la visionneuse de formulaires peut composer le message dans n'importe quel dossier. Si la variable a la valeur TRUE et si NULL est transmis dans le paramètre _pFolderFocus_ , le message est composé dans le dossier actif. Si la variable est TRUE et qu'une valeur non NULL est transmise dans _pFolderFocus_, le message est composé dans le dossier désigné par _pFolderFocus_.
    
 _pFolderFocus_
  
> dans Pointeur vers le dossier où le nouveau message est créé.
    
 _pPersistMessage_
  
> dans Pointeur vers l'objet de formulaire pour le nouveau formulaire.
    
 _ppMessage_
  
> remarquer Pointeur vers un pointeur vers le nouveau message.
    
 _ppMessageSite_
  
> remarquer Pointeur vers un pointeur vers un objet de site de message pour le nouveau message.
    
 _ppViewContext_
  
> remarquer Pointeur vers un pointeur vers un contexte d'affichage qui est approprié pour passer à un nouveau formulaire avec le nouveau message. Si le formulaire implémente son propre contexte d'affichage, la valeur NULL peut être transmise au paramètre _ppViewContext_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIMessageSite:: newMessage,** pour créer un message. Le formulaire utilise **newMessage,** pour obtenir un nouveau message et le site de messages associé à partir de sa vue. Il peut ensuite modifier le nouveau message. 
  
Vous pouvez également obtenir un contexte de vue associé en transmettant une valeur non NULL dans le paramètre _ppViewContext_ . Ce contexte d'affichage peut être utilisé directement, ou il peut être regroupé et transmis au nouveau message. Si une implémentation complète est requise, transmettez la valeur NULL dans _ppViewContext_.
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: newMessage,  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite:: newMessage,** pour créer un nouveau message, instancier une nouvelle visionneuse de formulaires et appeler **SetPersist** pour définir le message dans la visionneuse de formulaire. Enfin, il renvoie la visionneuse de formulaires en tant que site de messagerie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

