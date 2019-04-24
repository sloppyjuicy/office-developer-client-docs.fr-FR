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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351120"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère un flux à utiliser pour enregistrer le message actif.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Paramètres

 _pulFlags_
  
> remarquer Pointeur vers un masque de des indicateurs qui contrôle la manière dont le texte du message doit être enregistré. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Le texte du message est enregistré au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le texte est enregistré au format ANSI.
    
 _pulFormat_
  
> remarquer Pointeur vers un masque de des indicateurs qui contrôle le format du texte enregistré. Les indicateurs suivants peuvent être définis:
    
SAVE_FORMAT_RICHTEXT 
  
> Le texte du message doit être enregistré sous forme de texte mis en forme au format RTF (Rich Text Format). 
    
SAVE_FORMAT_TEXT 
  
> Le texte du message doit être enregistré en tant que texte brut. 
    
 _ppstm_
  
> remarquer Pointeur vers un pointeur vers le flux qui contiendra le message enregistré.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le flux a été correctement récupéré.
    
## <a name="remarks"></a>Remarques

Les objets Form appellent la méthode **IMAPIViewContext:: GetSaveStream** pour récupérer un objet qui implémente l'interface **IStream** afin de prendre en charge la gestion du verbe enregistrer sous dans la visionneuse de formulaires. La méthode [IMAPIForm::D overb](imapiform-doverb.md) , qui est implémentée dans le serveur de formulaires et appelée par la visionneuse de formulaires pour appeler un verbe, ne doit pas retourner tant que le message n'est pas entièrement converti au format de texte approprié et placé dans le flux approprié. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

N'écrivez pas dans le flux vers lequel pointe _ppstm_ avant d'appeler **GetSaveStream**. Lorsque **GetSaveStream** renvoie, ne réinitialisez pas la position du pointeur de recherche. Ce pointeur doit rester à la fin du texte du message enregistré. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

