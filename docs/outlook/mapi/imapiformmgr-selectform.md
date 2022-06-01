---
title: IMAPIFormMgrSelectForm
description: IMAPIFormMgrSelectForm présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations de formulaire qui décrit ce formulaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
ms.openlocfilehash: 8f62c1e5bed4e329d2cb2d4e33dc1d4deb0b5e80
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817850"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations de formulaire qui décrit ce formulaire.
  
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
  
> [in] Handle de la fenêtre parente de la boîte de dialogue affichée. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type des chaînes passées. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
 _pszTitle_
  
> [in] Pointeur vers une chaîne qui contient la légende de la boîte de dialogue. Si le paramètre  _pszTitle_ a la valeur NULL, le fournisseur de bibliothèque de formulaires fournit une légende par défaut. 
    
 _pfld_
  
> [in] Pointeur vers le dossier à partir duquel sélectionner le formulaire. Si le paramètre  _pfld_ est NULL, le formulaire peut être sélectionné à partir du conteneur de formulaires local, personnel ou d’organisation. 
    
 _ppfrminfoReturned_
  
> [out] Pointeur vers un pointeur vers l’objet d’informations de formulaire retourné.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::SelectForm** pour présenter d’abord une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire, puis de récupérer un objet d’informations de formulaire qui décrit le formulaire sélectionné. La boîte de dialogue contraint l’utilisateur à sélectionner un formulaire unique. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La boîte **de dialogue SelectForm** affiche uniquement les formulaires qui ne sont pas masqués (autrement dit, les formulaires dont les propriétés masquées sont claires). Si une visionneuse de formulaires passe l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont Unicode. Les fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent retourner MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::SelectForm** pour sélectionner un formulaire et envoyer des informations sur le formulaire à un ou plusieurs journaux d’activité. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

