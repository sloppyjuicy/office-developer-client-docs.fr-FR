---
title: IMAPIFormInfoCalcVerbSet
description: Décrit la syntaxe, les paramètres et la valeur de retour pour IMAPIFormInfoCalcVerbSet, qui retourne un pointeur vers l’ensemble complet de verbes qu’un formulaire utilise.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
ms.openlocfilehash: 41cb5d839c2971a9ab034c5f96127631c2ea28f3
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815666"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers l’ensemble complet de verbes qu’un formulaire utilise.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type de chaînes retournées. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
 _ppMAPIVerbArray_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIVerbArray](smapiverbarray.md) retournée qui contient les verbes du formulaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormInfo::CalcVerbSet** pour obtenir un pointeur vers l’ensemble de verbes utilisés par un formulaire. Dans la structure **SMAPIVerbArray** retournée dans le paramètre _ppMAPIVerbArray_ , les verbes sont retournés par ordre de numéro d’index ; L’index de chaque verbe se trouve dans son membre **lVerb** . Les applications clientes peuvent utiliser le tableau de verbes pour générer dynamiquement des menus, masquer ou afficher des boutons, et ainsi de suite. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI utilise la méthode **IMAPIFormInfo::CalcVerbSet** lors de l’écriture d’une sortie de débogage pour les objets d’informations de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

