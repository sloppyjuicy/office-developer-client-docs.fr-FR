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
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321636"
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
  
> dans Une énumération HFRMREG qui indique la bibliothèque de formulaires à ouvrir (autrement dit, le conteneur de formulaire à ouvrir). Une énumération HFRMREG est une énumération spécifique à un fournisseur de bibliothèque de formulaires. Les valeurs possibles de HFRMREG sont les suivantes:
    
HFRMREG_DEFAULT 
  
> Un conteneur de formulaire pratique.
    
HFRMREG_FOLDER 
  
> Conteneur de dossier. 
    
HFRMREG_PERSONAL 
  
> Conteneur de la Banque de messages par défaut. 
    
HFRMREG_LOCAL 
  
> Conteneur de formulaire local. 
    
 _lpUnk_
  
> dans Pointeur vers l'objet pour lequel l'interface est ouverte. Le paramètre _lpUnk_ doit être **null** , sauf si la valeur du paramètre _hfrmreg_ nécessite un pointeur d'objet. 
    
 _lppfcnt_
  
> remarquer Pointeur vers un pointeur vers l'objet conteneur de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L'objet pointé par _lpUnk_ ne prend pas en charge l'interface requise. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: OpenFormContainer** pour ouvrir une interface **IMAPIFormContainer** pour un conteneur de formulaire spécifique. Cette interface peut ensuite être utilisée pour installer des formulaires dans et supprimer des formulaires d'un conteneur de formulaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si la valeur de _hfrmreg_ est HFRMREG_FOLDER, l'identificateur d'interface utilisé dans _lpUnk_ doit être non **null** et doit autoriser les appels de méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) à une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Pour ouvrir le conteneur de formulaire local, vous devez utiliser un appel à la méthode **OpenFormContainer** ou à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; vous ne pouvez pas utiliser la méthode [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) pour permettre à l'utilisateur de sélectionner le conteneur de formulaire local. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr:: OpenFormContainer** pour récupérer un conteneur de formulaire afin que le contenu du conteneur puisse être rendu.  <br/> |
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnOpenFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr:: OpenFormContainer** pour récupérer un conteneur de formulaire pour un dossier, afin que le contenu du conteneur puisse être rendu.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

