---
title: MAPIOpenFormMgr
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8df25eade1065adc198bc356ffa4c96434de0b18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595762"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet fournisseur de bibliothèque de formulaires dans le contexte d’une session existante. 
  
|||
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
  
> [in] Pointeur vers la session en cours d’utilisation par l’application cliente.
    
 _ppmgr_
  
> [out] Pointeur vers l’interface **IMAPIFormMgr** renvoyée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Après qu’une application cliente a appelé la fonction **MAPIOpenFormMgr,** la plupart des interactions ultérieures liées aux formulaires ont lieu via le fournisseur de bibliothèque de formulaires ou une interface renvoyée par le fournisseur de bibliothèque de formulaires. **L’interface IMAPIFormMgr** permet au client d’utiliser des gestions de messages et d’effectuer des résolutions entre les classes de messages et les bibliothèques de formulaires. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp ouvre le gestionnaire de formulaires afin qu’un formulaire puisse être sélectionné.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI utilise la **méthode MAPIOpenFormMgr** pour ouvrir le gestionnaire de formulaire afin qu’un formulaire puisse être sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

