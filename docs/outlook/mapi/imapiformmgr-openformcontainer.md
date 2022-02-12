---
title: IMAPIFormMgrOpenFormContainer
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5d2f2511f9c86382ce6d88d84abeec25e5bc6c76
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773508"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Une éumération HFRMREG qui indique la bibliothèque de formulaires à ouvrir (autrement dit, le conteneur de formulaire à ouvrir). Une éumération HFRMREG est une éumération spécifique à un fournisseur de bibliothèque de formulaires. Les valeurs HFRMREG possibles sont les suivantes :
    
HFRMREG_DEFAULT 
  
> Conteneur de formulaires pratique.
    
HFRMREG_FOLDER 
  
> Conteneur de dossiers. 
    
HFRMREG_PERSONAL 
  
> Conteneur de la magasin de messages par défaut. 
    
HFRMREG_LOCAL 
  
> Conteneur de formulaire local. 
    
 _lpunk_
  
> [in] Pointeur vers l’objet pour lequel l’interface est ouverte. Le  _paramètre lpunk_ doit être **null** , sauf si la valeur du paramètre  _hfrmreg_ nécessite un pointeur d’objet. 
    
 _lppfcnt_
  
> [out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L’objet pointé par  _lpunk_ ne prend pas en charge l’interface requise. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::OpenFormContainer** pour ouvrir une interface **IMAPIFormContainer** pour un conteneur de formulaire spécifique. Cette interface peut ensuite être utilisée pour installer et supprimer des formulaires dans un conteneur de formulaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si la valeur dans  _hfrmreg_ est HFRMREG_FOLDER, l’identificateur d’interface utilisé dans  _lpunk_ doit être **non null et** autoriser les appels de méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) à une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Pour ouvrir le conteneur de formulaires local, vous devez utiliser un appel à la méthode **OpenFormContainer** ou à la [fonction MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; vous ne pouvez pas utiliser [la méthode IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour permettre à l’utilisateur de sélectionner le conteneur de formulaire local. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire afin que le contenu du conteneur puisse être rendu. |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire pour un dossier afin que le contenu du conteneur puisse être rendu. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

