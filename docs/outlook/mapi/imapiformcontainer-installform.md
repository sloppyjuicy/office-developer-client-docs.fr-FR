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
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche. Le paramètre _ulUIParam_ est ignoré sauf si l'application cliente définit l'indicateur MAPI_DIALOG dans le paramètre _ulFlags_ . Le paramètre _ulUIParam_ peut être null si MAPI_DIALOG n'est pas également passé. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'installation du formulaire. Les indicateurs suivants peuvent être définis:
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue qui fournit des informations d'avancement ou invite l'utilisateur à fournir des informations supplémentaires. Si cet indicateur n'est pas défini, aucune boîte de dialogue ne s'affiche.
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> S'il existe déjà un autre formulaire qui gère la classe de message gérée par ce formulaire, remplacez le formulaire existant par celui-ci. Cet indicateur est ignoré si l'indicateur MAPI_DIALOG est également présent. 
    
 _szCfgPathName_
  
> dans Chemin d'accès au fichier de configuration du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_EXTENDED_ERROR 
  
> Une erreur d'implémentation s'est produite. Pour obtenir la structure [MAPIERROR](mapierror.md) associée à l'erreur, appelez la méthode [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'installation du formulaire, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de bibliothèques de formulaires doivent remplir une structure **MAPIERROR** et renvoyer MAPI_E_EXTENDED_ERROR si l'une des conditions suivantes se produit: 
  
- Le fichier de configuration est introuvable.
    
- Le fichier de configuration n'est pas lisible.
    
- Le fichier de configuration n'est pas valide.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les applications clientes appellent la méthode **IMAPIFormContainer:: InstallForm** pour installer un formulaire dans un conteneur de formulaire spécifique. Le paramètre _szCfgPathName_ doit contenir le chemin d'accès d'un fichier de configuration de formulaire (c'est-à-dire un fichier doté de l'extension. cfg qui décrit le formulaire et son implémentation). Les indicateurs dans le paramètre _ulFlags_ spécifient les éléments suivants: 
  
- Si l'indicateur MAPI_DIALOG est défini, une interface utilisateur s'affiche, ce qui permet à l'utilisateur qui installe le formulaire de spécifier les détails de l'installation.
    
- Si l'indicateur MAPIFORM_INSTALL_OVERWRITEONCONFLICT est défini, tout formulaire précédent pour la même classe de message est remplacé par le formulaire en cours d'installation. Dans le cas contraire, l'installation du formulaire est fusionnée avec la description de formulaire actuelle, si elle existe.
    
- Si MAPI_DIALOG est défini, MAPIFORM_INSTALL_OVERWRITEONCONFLICT est ignoré.
    
- L'absence de MAPIFORM_INSTALL_OVERWRITEONCONFLICT dans l'ensemble d'indicateurs signifie qu'une fusion sera réalisée. Toutes les nouvelles plateformes du fichier. cfg qui ne sont pas présentes dans la description du formulaire sont installées et aucune autre modification n'est effectuée.
    
- Si l'indicateur MAPI_UNICODE est défini, le chemin d'accès au fichier de configuration du formulaire est une chaîne Unicode. 
    
Les clients doivent appeler [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** renvoie MAPI_E_EXTENDED_ERROR et vérifier la structure [MAPIERROR](mapierror.md) renvoyée pour déterminer la condition à l'origine de l'erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnInstallForm  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer:: InstallForm** pour installer un formulaire dans un conteneur de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

