---
title: IMAPIMessageSiteGetStore
description: IMAPIMessageSiteGetStore retourne le magasin de messages qui contient le message actuel, s’il existe un tel magasin.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
ms.openlocfilehash: a84b01a49dc21fffab6adbacbb4b6e7950bd1785
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816835"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne le magasin de messages qui contient le message actuel, s’il existe un tel magasin. Cette méthode retourne null dans le paramètre _ppStore_ pour les messages incorporés, qui sont stockés dans un autre message plutôt que directement dans un magasin de messages. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Paramètres

 _ppStore_
  
> [out] Pointeur vers un pointeur vers le magasin de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
S_FALSE 
  
> Il n’existe aucun magasin qui contient le message.
    
## <a name="remarks"></a>Remarques

Pour obtenir la liste des interfaces liées aux serveurs de formulaires, consultez [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetStore** pour obtenir le pointeur actuellement mis en cache vers le magasin spécifié, s’il est disponible. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

