---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784125"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**S’applique à**: Outlook 
  
Récupère un flux de données à utiliser pour l’enregistrement du message en cours.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Paramètres

 _pulFlags_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui contrôle la façon dont le texte du message doit être enregistré. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Le texte du message est enregistré au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le texte est enregistré au format ANSI.
    
 _pulFormat_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui contrôle le format du texte enregistré. Les indicateurs suivants peuvent être définis :
    
SAVE_FORMAT_RICHTEXT 
  
> Le texte du message doit être enregistré en tant que texte mis en forme dans le Format de texte enrichi (RTF). 
    
SAVE_FORMAT_TEXT 
  
> Le texte du message doit être enregistré en tant que texte brut. 
    
 _ppstm_
  
> [out] Pointeur vers un pointeur vers le flux qui contiendra le message enregistré.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le flux de données a été récupéré correctement.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIViewContext::GetSaveStream** pour récupérer un objet qui implémente l’interface **IStream** pour prendre en charge la gestion de l’action Enregistrer sous dans la visionneuse de formulaire de flux. La méthode [IMAPIForm::DoVerb](imapiform-doverb.md) , qui est implémentée sous la forme et appelée par la visionneuse de formulaire pour appeler un verbe, ne doit pas renvoyer jusqu'à ce que le message est entièrement converti au format texte approprié et placé dans le flux approprié. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Ne pas écrire dans le flux indiqué par _ppstm_ avant d’appeler **GetSaveStream**. Lorsque **GetSaveStream** renvoie, ne pas réinitialiser la position du pointeur de la recherche. Ce pointeur doit rester à la fin du texte du message enregistré. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

