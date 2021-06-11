---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410468"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la magasine de messages qui contient le message actuel, si tel est le cas. Cette méthode retourne null dans le paramètre  _ppStore_ pour les messages incorporés, qui sont stockés dans un autre message plutôt que directement dans une magasin de messages. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Parameters

 _ppStore_
  
> [out] Pointeur vers un pointeur vers la magasin de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
S_FALSE 
  
> Il n’existe pas de magasin contenant le message.
    
## <a name="remarks"></a>Remarques

Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetStore** pour obtenir le pointeur actuellement mis en cache vers la boutique spécifiée, si elle est disponible.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

