---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f5d7c8031dfcf6a0142603205eb9a334806a1067
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773403"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demande que le message actuel soit enregistré.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucun.
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
## <a name="remarks"></a>Remarques

Les formulaires **appellent la méthode IMAPIMessageSite::SaveMessage** pour demander qu’un message soit enregistré. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [INTERFACES DE FORMULAIRE MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SaveMessage  <br/> |MFCMAPI utilise la **méthode IMAPIMessageSite::SaveMessage** pour enregistrer le message. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

