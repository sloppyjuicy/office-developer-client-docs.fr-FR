---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321594"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche une boîte de dialogue qui permet à l'utilisateur de sélectionner plusieurs formulaires et renvoie un tableau d'objets d'informations de formulaire qui décrivent ces formulaires.
  
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
  
> dans Handle de la fenêtre parent de la boîte de dialogue affichée. 
    
 _ulFlags_
  
> dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _pszTitle_
  
> dans Pointeur vers une chaîne qui contient la légende de la boîte de dialogue. Si le paramètre _pszTitle_ est null, le fournisseur de bibliothèque de formulaires qui fournit les formulaires fournit une légende par défaut. 
    
 _pfld_
  
> dans Pointeur vers le dossier à partir duquel sélectionner les formulaires. Si le paramètre _pfld_ est null, les formulaires sont sélectionnés à partir du conteneur de formulaire local, personnel ou organisation. 
    
 _pfrminfoarray_
  
> dans Pointeur vers un tableau d'objets d'informations de formulaire présélectionnés pour l'utilisateur.
    
 _ppfrminfoarray_
  
> remarquer Pointeur vers un pointeur vers le tableau renvoyé d'objets d'informations de formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: SelectMultipleForms** pour commencer par présenter une boîte de dialogue qui permet à l'utilisateur de sélectionner plusieurs formulaires, puis de récupérer un tableau d'objets d'informations de formulaire qui décrivent les formulaires sélectionnés. La boîte de dialogue **SelectMultipleForms** affiche tous les formulaires, qu'ils soient ou non masqués (c'est-à-dire, si leurs propriétés masquées sont claires ou non). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si une visionneuse de formulaires transmet l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont au format Unicode. Les fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est transmis. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

