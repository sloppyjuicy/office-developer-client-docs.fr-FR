---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 898c5fd237d9a9654d3ac3a100ac2bbaf298b20c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773424"
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
  
> [in] Indique dans quel dossier le message doit être composé. Si la variable est FALSE, le paramètre  _pFolderFocus_ est ignoré et la visionneuse de formulaires peut composer le message dans n’importe quel dossier. Si la variable est TRUE et que null est transmis dans le paramètre _pFolderFocus_ , le message est composé dans le dossier actuel. Si la variable est TRUE et qu’une valeur non NULL est transmise dans  _pFolderFocus_, le message est composé dans le dossier pointé par  _pFolderFocus_.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier dans lequel le nouveau message est créé.
    
 _pPersistMessage_
  
> [in] Pointeur vers l’objet de formulaire pour le nouveau formulaire.
    
 _ppMessage_
  
> [out] Pointeur vers un pointeur vers le nouveau message.
    
 _ppMessageSite_
  
> [out] Pointeur vers un pointeur vers un objet de site de message pour le nouveau message.
    
 _ppViewContext_
  
> [out] Pointeur vers un pointeur vers un contexte d’affichage approprié pour la transmission vers un nouveau formulaire avec le nouveau message. Si le formulaire implémente son propre contexte d’affichage, NULL peut être transmis dans le _paramètre ppViewContext_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les objets form appellent **la méthode IMAPIMessageSite::NewMessage** pour créer un message. Le formulaire utilise **NewMessage pour** obtenir un nouveau message et le site de message associé à partir de son affichage. Il peut ensuite modifier le nouveau message. 
  
Vous pouvez également obtenir un contexte d’affichage associé en passant une valeur non NULL dans le _paramètre ppViewContext_ . Ce contexte d’affichage peut être utilisé directement, ou il peut être agrégé et transmis au nouveau message. Si une implémentation complète est requise, passez NULL dans  _ppViewContext_.
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [INTERFACES DE FORMULAIRE MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::NewMessage** pour créer un message, inssérer une nouvelle visionneuse de formulaires et appeler **SetPersist** pour définir le message sur la visionneuse de formulaires. Enfin, elle renvoie la visionneuse de formulaires en tant que site de message. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

