---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784751"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**S’applique à**: Outlook 
  
Ouvre une interface [IMAPIFormMgr](imapiformmgriunknown.md) sur un objet de fournisseur de bibliothèque formulaire dans le contexte d’une session existante. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [out] Pointeur vers l’interface **IMAPIFormMgr** retournée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une fois une application cliente effectue un appel à la fonction **MAPIOpenFormMgr** , la plupart des interactions de basés sur des formulaires suivants ont lieu via le fournisseur de bibliothèque de formulaire ou d’une interface renvoyée par le fournisseur de bibliothèque de formulaires. L’interface **IMAPIFormMgr** autorise le client à travailler avec les gestionnaires de messages et effectuer des résolutions entre les classes de message et des bibliothèques de formulaires. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp ouvre le Gestionnaire de formulaire pour un formulaire peut être sélectionné.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI utilise la méthode **MAPIOpenFormMgr** pour ouvrir le Gestionnaire de formulaire pour un formulaire peut être sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

