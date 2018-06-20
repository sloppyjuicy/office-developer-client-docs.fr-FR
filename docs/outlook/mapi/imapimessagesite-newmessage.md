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
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783847"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**S’applique à**: Outlook 
  
Crée un nouveau message.
  
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
  
> [in] Indique le dossier dans lequel le message doit être composé. Si la variable a la valeur FALSE, le paramètre _pFolderFocus_ est ignoré et la visionneuse de formulaire permettre composer le message dans un dossier. Si la variable a la valeur TRUE et NULL est passé dans le paramètre _pFolderFocus_ , le message est composé dans le dossier actif. Si la variable a la valeur TRUE et une valeur non nulle est passée _pFolderFocus_, le message se compose dans le dossier désigné par _pFolderFocus_.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier dans lequel le nouveau message est créé.
    
 _pPersistMessage_
  
> [in] Pointeur vers l’objet de formulaire pour le nouveau formulaire.
    
 _ppMessage_
  
> [out] Pointeur vers un pointeur vers le nouveau message.
    
 _ppMessageSite_
  
> [out] Pointeur vers un pointeur vers un objet de site de message du nouveau message.
    
 _ppViewContext_
  
> [out] Pointeur vers un pointeur vers un contexte de vue est approprié pour passer à un nouveau formulaire avec le nouveau message. Si le formulaire implémente son propre contexte de vue, NULL peut être passé dans le paramètre _ppViewContext_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIMessageSite::NewMessage** pour créer un nouveau message. Le formulaire utilise **NewMessage** pour obtenir un nouveau message et le site de message associé à partir de son affichage. Il peut ensuite modifier le nouveau message. 
  
Vous pouvez également obtenir un contexte de la vue associée en transmettant une valeur non NULL dans le paramètre _ppViewContext_ . Ce contexte de vue peut être utilisé directement, ou pouvant être regroupé et transmis vers le nouveau message. Si une implémentation complète est requise, passez la valeur NULL dans _ppViewContext_.
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::NewMessage** pour créer un nouveau message, instanciez un nouvel Observateur de formulaire et appeler **SetPersist** pour définir le message de la visionneuse de formulaire. Enfin, elle renvoie la visionneuse de formulaire en tant que le site de message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

