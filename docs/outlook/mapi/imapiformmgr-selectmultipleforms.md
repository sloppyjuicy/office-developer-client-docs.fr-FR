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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b974b733c24e61cb256ac0cf7b377d5630966fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579290"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et renvoie un tableau de formulaire objets informations décrivant les formulaires.
  
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
  
> [in] Handle vers la fenêtre parente de la boîte de dialogue qui s’affiche. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _pszTitle_
  
> [in] Pointeur vers une chaîne qui contient la légende de la boîte de dialogue. Si le paramètre _pszTitle_ est NULL, le fournisseur de bibliothèque de formulaires qui fournit les formulaires fournit une légende par défaut. 
    
 _pfld_
  
> [in] Pointeur vers le dossier à partir desquels sélectionner les formulaires. Si le paramètre _pfld_ est NULL, les formulaires sont sélectionnées dans le conteneur de formulaire local, personnel ou organisation. 
    
 _pfrminfoarray_
  
> [in] Pointeur vers un tableau d’objets d’informations de formulaire qui sont présélectionnés pour l’utilisateur.
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers le tableau d’objets formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appellent la méthode de **IMAPIFormMgr::SelectMultipleForms** au premier présente une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et puis pour récupérer un tableau de formulaire d’informations des objets qui décrivent les formulaires sélectionnés. La boîte de dialogue **SelectMultipleForms** affiche tous les formulaires, si elles sont masquées (autrement dit, si leurs propriétés masquées sont claires). 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si une visionneuse de formulaire transmet l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont en Unicode. Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

