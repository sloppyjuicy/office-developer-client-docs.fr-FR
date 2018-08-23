---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d5d86af111bc778839a78f9b56ba7126e6c973d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567376"
---
# <a name="imapimessagesitegetsession"></a>IMAPIMessageSite::GetSession

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie la session MAPI dans lequel le message en cours a été créé ou ouvert.
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a>Paramètres

 _ppSession_
  
> [out] Pointeur vers un pointeur vers l’objet de session retourné.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
S_FALSE 
  
> Aucune session n’existe pour le message en cours.
    
## <a name="remarks"></a>Remarques

Pour obtenir la liste des interfaces qui sont liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetSession** pour renvoyer le pointeur de la session actuellement mis en cache, s’il est disponible.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

