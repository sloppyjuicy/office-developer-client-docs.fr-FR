---
title: IMAPIFormMgrOpenFormContainer
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIFormMgrOpenFormContainer, qui ouvre une interface IMAPIFormContainer pour un conteneur de formulaires spécifique.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
ms.openlocfilehash: 612a0d2859a6ac76eb90ff5cf0523e96556b700e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812179"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaires spécifique. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Paramètres

 _hfrmreg_
  
> [in] Énumération HFRMREG qui indique la bibliothèque de formulaires à ouvrir (autrement dit, le conteneur de formulaires à ouvrir). Une énumération HFRMREG est une énumération spécifique à un fournisseur de bibliothèque de formulaires. Les valeurs HFRMREG possibles sont les suivantes :
    
HFRMREG_DEFAULT 
  
> Un conteneur de formulaires pratique.
    
HFRMREG_FOLDER 
  
> Conteneur de dossiers. 
    
HFRMREG_PERSONAL 
  
> Conteneur du magasin de messages par défaut. 
    
HFRMREG_LOCAL 
  
> Conteneur de formulaires local. 
    
 _lpunk_
  
> [in] Pointeur vers l’objet pour lequel l’interface est ouverte. Le paramètre  _lpunk_ doit être **null** , sauf si la valeur du paramètre  _hfrmreg_ nécessite un pointeur d’objet. 
    
 _lppfcnt_
  
> [out] Pointeur vers un pointeur vers l’objet conteneur de formulaire retourné.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L’objet pointé par  _l lui_ ne prend pas en charge l’interface requise. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::OpenFormContainer** pour ouvrir une interface **IMAPIFormContainer** pour un conteneur de formulaire spécifique. Cette interface peut ensuite être utilisée pour installer et supprimer des formulaires d’un conteneur de formulaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si la valeur dans  _hfrmreg_ est HFRMREG_FOLDER, l’identificateur d’interface utilisé dans  _lmv_ doit être non **null** et doit autoriser les appels de méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) à une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Pour ouvrir le conteneur de formulaires local, vous devez utiliser un appel à la méthode **OpenFormContainer** ou à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; vous ne pouvez pas utiliser la méthode [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour permettre à l’utilisateur de sélectionner le conteneur de formulaires local. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaires afin que le contenu du conteneur puisse être affiché. |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaires pour un dossier afin que le contenu du conteneur puisse être affiché. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

