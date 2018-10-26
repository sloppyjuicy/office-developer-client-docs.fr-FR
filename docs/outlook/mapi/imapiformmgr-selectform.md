---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3c6242c9a926341908cb86645a8ea8586a9ca598
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586353"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations de formulaire qui décrit ce formulaire.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de la boîte de dialogue qui s’affiche. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _pszTitle_
  
> [in] Pointeur vers une chaîne qui contient la légende de la boîte de dialogue. Si le paramètre _pszTitle_ est NULL, le fournisseur de bibliothèque formulaire fournit une légende par défaut. 
    
 _pfld_
  
> [in] Pointeur vers le dossier à partir desquels sélectionner le formulaire. Si le paramètre _pfld_ est NULL, le formulaire peut être sélectionné à partir du conteneur de formulaire local, personnel ou organisation. 
    
 _ppfrminfoReturned_
  
> [out] Pointeur vers un pointeur vers l’objet d’informations de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appellent la méthode **IMAPIFormMgr::SelectForm** à présent premier une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et puis pour récupérer un objet d’informations de formulaire qui décrit le formulaire sélectionné. La boîte de dialogue contraint l’utilisateur de sélectionner un seul formulaire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La boîte de dialogue **SelectForm** n’affiche que les formulaires qui ne sont pas masqués (autrement dit, désactivez les formulaires qui disposent de leurs propriétés masquées). Si une visionneuse de formulaire transmet l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont en Unicode. Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::SelectForm** pour sélectionner un formulaire et envoyer des informations sur le formulaire à un ou plusieurs journaux.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

