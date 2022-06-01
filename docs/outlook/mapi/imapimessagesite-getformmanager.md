---
title: IMAPIMessageSiteGetFormManager
description: IMAPIMessageSiteGetFormManager retourne une interface de gestionnaire de formulaires, qu’un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
ms.openlocfilehash: 2d97ce4638fee4386d2136598bf01f78ec8a4cde
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815645"
---
# <a name="imapimessagesitegetformmanager"></a>IMAPIMessageSite::GetFormManager

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne une interface du gestionnaire de formulaires, qu’un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires.
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a>Paramètres

 _ppFormMgr_
  
> [out] Pointeur vers un pointeur vers l’interface du gestionnaire de formulaires retournée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Pour obtenir la liste des interfaces liées aux serveurs de formulaires, consultez [Interfaces de formulaire MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFormManager  <br/> |MFCMAPI utilise la méthode **IMAPIMessageSite::GetFormManager** pour appeler [MAPIOpenFormMgr](mapiopenformmgr.md) et retourner les résultats de cet appel. |
   
## <a name="see-also"></a>Voir aussi



[MAPIOpenFormMgr](mapiopenformmgr.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulaire MAPI](mapi-form-interfaces.md)

