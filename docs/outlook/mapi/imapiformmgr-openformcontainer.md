---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 64031725e06a949464e7bfabb0a2f114d325470e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783805"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**S’applique à**: Outlook 
  
Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Paramètres

 _hfrmreg_
  
> [in] Énumération HFRMREG indiquant la bibliothèque de formulaires pour ouvrir (autrement dit, le conteneur de formulaire à ouvrir). Énumération HFRMREG est une énumération qui est spécifique à un fournisseur de bibliothèque de formulaires. Les valeurs HFRMREG possibles sont les suivantes :
    
HFRMREG_DEFAULT 
  
> Un conteneur pratique de formulaire.
    
HFRMREG_FOLDER 
  
> Un conteneur de dossiers. 
    
HFRMREG_PERSONAL 
  
> Conteneur pour la banque de messages par défaut. 
    
HFRMREG_LOCAL 
  
> Conteneur formulaire local. 
    
 _lpUnk_
  
> [in] Pointeur vers l’objet pour lequel l’interface est ouvert. Le paramètre _lpunk_ doit être **null** , sauf si la valeur pour le paramètre _hfrmreg_ nécessite un pointeur d’objet. 
    
 _lppfcnt_
  
> [out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L’objet vers lequel pointé _lpunk_ ne prend pas en charge l’interface requise. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::OpenFormContainer** pour ouvrir une interface **IMAPIFormContainer** pour un conteneur de formulaire spécifique. Cette interface puis peut être utilisée pour l’installation dans et la suppression de formulaires à partir d’un conteneur de formulaire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si la valeur de _hfrmreg_ est HFRMREG_FOLDER, l’identificateur d’interface utilisé dans _lpunk_ doit être non **null** et doit autoriser les appels de méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) vers une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Pour ouvrir le conteneur de formulaire local, vous devez utiliser un appel à la méthode **OpenFormContainer** ou la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; Vous ne pouvez pas utiliser la méthode [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour permettre à l’utilisateur sélectionner le conteneur de formulaire local. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire afin que le contenu du conteneur peut être affiché.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire pour un dossier afin que le contenu du conteneur peut être affiché.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

