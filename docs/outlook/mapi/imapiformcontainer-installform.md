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
ms.openlocfilehash: fd7bc8f051e9584fc63f22bdbaf9696c2e4d15a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580935"
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode. Le paramètre _ulUIParam_ est ignoré à moins que l’application cliente définit l’indicateur MAPI_DIALOG dans le paramètre _ulFlags_ . Le paramètre _ulUIParam_ peut être NULL si MAPI_DIALOG n’est pas également transmises. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’installation du formulaire. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue pour fournir des informations d’avancement ou demander à l’utilisateur pour plus d’informations. Si cet indicateur n’est pas défini, aucune boîte de dialogue ne s’affiche.
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Si un autre formulaire existe déjà qui gère la classe de message gérée par ce formulaire, remplacer le formulaire existant par celui-ci. Cet indicateur est ignoré si l’indicateur MAPI_DIALOG est également présent. 
    
 _szCfgPathName_
  
> [in] Le chemin d’accès au fichier de configuration du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_EXTENDED_ERROR 
  
> Erreur d’implémentation. Pour obtenir la structure [MAPIERROR](mapierror.md) qui est associée à l’erreur, appelez la méthode [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’installation du formulaire, de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Fournisseurs de bibliothèques de formulaires doivent remplir une structure **MAPIERROR** et renvoyer MAPI_E_EXTENDED_ERROR si une des conditions suivantes se produisent : 
  
- Le fichier de configuration est introuvable.
    
- Le fichier de configuration n’est pas lisible.
    
- Le fichier de configuration n’est pas valide.
    
## <a name="notes-to-callers"></a>Notes aux appelants

Applications clientes appellent la méthode **IMAPIFormContainer::InstallForm** pour installer un formulaire dans un conteneur de formulaire spécifique. Le paramètre _szCfgPathName_ doit contenir le chemin d’accès d’un fichier de configuration de formulaire (autrement dit, un fichier avec l’extension .cfg qui décrit le formulaire et son implémentation). Les indicateurs dans le paramètre _ulFlags_ spécifient les éléments suivants : 
  
- Si l’indicateur MAPI_DIALOG est défini, une interface utilisateur s’affiche, permettant à l’utilisateur qui installe le formulaire pour spécifier les détails de l’installation.
    
- Si l’indicateur MAPIFORM_INSTALL_OVERWRITEONCONFLICT est défini, n’importe quel formulaire précédent pour la même classe de message est remplacée par le formulaire en cours d’installation. Dans le cas contraire, l’installation de formulaire est fusionnée avec la description du formulaire actif, si elle existe.
    
- Si la valeur MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT est ignorée.
    
- L’absence de MAPIFORM_INSTALL_OVERWRITEONCONFLICT dans l’indicateur défini signifie qu’une fusion sera effectuée. Les nouvelles plates-formes qui ne sont pas présents dans la description du formulaire dans le fichier .cfg seront installés et aucune autre modification n’aura lieu.
    
- Si l’indicateur MAPI_UNICODE est défini, le chemin d’accès du fichier de configuration du formulaire est une chaîne Unicode. 
    
Les clients doivent appeler [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** renvoie MAPI_E_EXTENDED_ERROR, et ils doivent vérifier la structure [MAPIERROR](mapierror.md) retournée pour déterminer la condition qui a déclenché l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::InstallForm** pour installer un formulaire dans un conteneur de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

