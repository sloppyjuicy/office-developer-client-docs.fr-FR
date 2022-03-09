---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
ms.openlocfilehash: 5e53bcc2741ae66cc055363b9f59b46f75bdf4e5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372597"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait un flux à utiliser pour enregistrer le message actuel.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Paramètres

 _graphieFlags_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui contrôle la façon dont le texte du message doit être enregistré. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Le texte du message est enregistré au format Unicode. Si l’MAPI_UNICODE n’est pas définie, le texte est enregistré au format ANSI.
    
 _atomFormat_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui contrôle le format du texte enregistré. Les indicateurs suivants peuvent être définies :
    
SAVE_FORMAT_RICHTEXT 
  
> Le texte du message doit être enregistré en tant que texte formaté au format RTF (Rich Text Format). 
    
SAVE_FORMAT_TEXT 
  
> Le texte du message doit être enregistré en tant que texte simple. 
    
 _ppstm_
  
> [out] Pointeur vers un pointeur vers le flux qui contiendra le message enregistré.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le flux a été récupéré avec succès.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIViewContext::GetSaveStream** pour récupérer un flux d’un objet qui implémente l’interface **IStream** pour prendre en charge la gestion du verbe Enregistrer sous dans la visionneuse de formulaires. La méthode [IMAPIForm::D oVerb](imapiform-doverb.md) , implémentée dans le serveur de formulaires et appelée par la visionneuse de formulaire pour appeler un verbe, ne doit pas renvoyer tant que le message n’a pas été entièrement converti au format de texte approprié et placé dans le flux approprié. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

N’écrivez pas dans le flux pointé par  _ppstm_ avant **d’appeler GetSaveStream**. Lorsque **GetSaveStream est de** retour, ne réinitialisez pas la position du pointeur de recherche. Ce pointeur doit rester à la fin du texte du message enregistré. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

