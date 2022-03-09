---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
ms.openlocfilehash: f817aa955ee439b18d32f983e339ab6527c82dc2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378672"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et renvoie un tableau d’objets d’informations sur les formulaires qui décrivent ces formulaires.
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue affichée. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes transmises. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _pszTitle_
  
> [in] Pointeur vers une chaîne qui contient la légende de la boîte de dialogue. Si le  _paramètre pszTitle_ est NULL, le fournisseur de bibliothèque de formulaires qui fournit les formulaires fournit une légende par défaut. 
    
 _pfld_
  
> [in] Pointeur vers le dossier à partir duquel sélectionner les formulaires. Si le  _paramètre pfld_ est NULL, les formulaires sont sélectionnés dans le conteneur de formulaires local, personnel ou d’organisation. 
    
 _pfrminfoarray_
  
> [in] Pointeur vers un tableau d’objets d’informations de formulaire pré-sélectionnés pour l’utilisateur.
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers le tableau renvoyé d’objets d’informations de formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le **bouton Annuler dans** la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::SelectMultipleForms** pour présenter d’abord une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires, puis de récupérer un tableau d’objets d’informations sur les formulaires qui décrivent les formulaires sélectionnés. La **boîte de dialogue SelectMultipleForms** affiche tous les formulaires, qu’ils soient masqués ou non (c’est-à-dire, si leurs propriétés masquées sont claires ou non). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si une visionneuse de formulaire passe l’MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont Unicode. Les fournisseurs de bibliothèques de formulaires qui ne prisent pas en charge les chaînes Unicode doivent MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

