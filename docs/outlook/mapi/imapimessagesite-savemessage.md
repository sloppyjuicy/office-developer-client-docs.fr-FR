---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9fa7c7226c4ddb5acf5c6b73f55c46829d959eef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572304"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Demandes d’enregistrer le message en cours.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucun.
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
## <a name="remarks"></a>Remarques

Formulaires appeler la méthode **IMAPIMessageSite::SaveMessage** pour demander qu’un message enregistré. 
  
Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SaveMessage  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::SaveMessage** pour enregistrer le message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

