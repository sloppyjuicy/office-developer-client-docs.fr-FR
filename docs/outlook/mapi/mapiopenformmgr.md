---
title: MAPIOpenFormMgr
description: Décrit la fonction MAPIOpenFormMgr et fournit la syntaxe, les paramètres, la valeur de retour, les remarques et la référence MFCMAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
ms.openlocfilehash: 1299a28802845ae24cbb5f7de3c1dd6ab95081be
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817472"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet fournisseur de bibliothèque de formulaires dans le contexte d’une session existante. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Paramètres

 _pSession_
  
> [in] Pointeur vers la session utilisée par l’application cliente.
    
 _ppmgr_
  
> [out] Pointeur vers l’interface **IMAPIFormMgr** retournée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une fois qu’une application cliente a appelé la fonction **MAPIOpenFormMgr** , la plupart des interactions suivantes liées aux formulaires ont lieu via le fournisseur de bibliothèque de formulaires ou une interface retournée par le fournisseur de bibliothèque de formulaires. **L’interface IMAPIFormMgr** permet au client d’utiliser des gestionnaires de messages et d’effectuer des résolutions entre les classes de messages et les bibliothèques de formulaires. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp ouvre le gestionnaire de formulaires afin qu’un formulaire puisse être sélectionné. |CMainDlg::OnSelectForm  <br/> |MFCMAPI utilise la méthode **MAPIOpenFormMgr** pour ouvrir le gestionnaire de formulaires afin qu’un formulaire puisse être sélectionné. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

