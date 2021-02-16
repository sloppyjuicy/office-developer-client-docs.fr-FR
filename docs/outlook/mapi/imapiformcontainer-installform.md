---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405085"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Installe un formulaire dans une bibliothèque de formulaires.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. Le _paramètre ulUIParam_ est ignoré, sauf si l’application cliente définit l’MAPI_DIALOG dans le _paramètre ulFlags._ Le  _paramètre ulUIParam_ peut être NULL si MAPI_DIALOG n’est pas également transmis. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’installation du formulaire. Les indicateurs suivants peuvent être définies :
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue pour fournir des informations sur l’avancement ou invite l’utilisateur à fournir plus d’informations. Si cet indicateur n’est pas définie, aucune boîte de dialogue n’est affichée.
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> S’il existe déjà un autre formulaire qui gère la classe de message gérée par ce formulaire, remplacez le formulaire existant par celui-ci. Cet indicateur est ignoré si l’MAPI_DIALOG est également présent. 
    
 _szCfgPathName_
  
> [in] Chemin d’accès au fichier de configuration du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_EXTENDED_ERROR 
  
> Une erreur d’implémentation s’est produite. Pour obtenir la structure [MAPIERROR](mapierror.md) associée à l’erreur, appelez la méthode [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md) 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’installation du formulaire, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de bibliothèques de formulaires doivent remplir une structure **MAPIERROR** et renvoyer MAPI_E_EXTENDED_ERROR si l’une des conditions suivantes se produit : 
  
- Le fichier de configuration est in trouvé.
    
- Le fichier de configuration n’est pas lisible.
    
- Le fichier de configuration n’est pas valide.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les applications clientes appellent **la méthode IMAPIFormContainer::InstallForm** pour installer un formulaire dans un conteneur de formulaire spécifique. Le  _paramètre szCfgPathName_ doit contenir le chemin d’accès d’un fichier de configuration de formulaire (autrement dit, un fichier avec l’extension .cfg qui décrit le formulaire et son implémentation). Les indicateurs du paramètre  _ulFlags_ spécifient les paramètres suivants : 
  
- Si l MAPI_DIALOG est définie, une interface utilisateur s’affiche, ce qui permet à l’utilisateur qui installe le formulaire de spécifier les détails de l’installation.
    
- Si l MAPIFORM_INSTALL_OVERWRITEONCONFLICT est définie, tout formulaire précédent pour la même classe de message est remplacé par le formulaire en cours d’installation. Dans le cas contraire, l’installation du formulaire est fusionnée avec la description du formulaire actuel, le cas contraire.
    
- Si MAPI_DIALOG est définie, MAPIFORM_INSTALL_OVERWRITEONCONFLICT est ignoré.
    
- L’absence de MAPIFORM_INSTALL_OVERWRITEONCONFLICT dans le jeu d’indicateurs signifie qu’une fusion sera effectuée. Toutes les nouvelles plateformes du fichier .cfg qui ne sont pas actuellement présentes dans la description du formulaire seront installées et aucune autre modification ne se produira.
    
- Si l MAPI_UNICODE est définie, le chemin d’accès du fichier de configuration du formulaire est une chaîne Unicode. 
    
Les clients doivent appeler [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** renvoie MAPI_E_EXTENDED_ERROR, et ils doivent vérifier la structure [MAPIERROR](mapierror.md) renvoyée pour déterminer la condition qui a renvoyé l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI utilise la **méthode IMAPIFormContainer::InstallForm** pour installer un formulaire dans un conteneur de formulaires.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

