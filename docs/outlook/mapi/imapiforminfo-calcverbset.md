---
title: IMAPIFormInfoCalcVerbSet
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b5755a587b2a2e0c708b2e7a828c8d5bad53b424
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784131"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers l’ensemble complet des verbes qu’un formulaire utilise.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _ppMAPIVerbArray_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIVerbArray](smapiverbarray.md) renvoyée qui contient les verbes du formulaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent **la méthode IMAPIFormInfo::CalcVerbSet** pour obtenir un pointeur vers l’ensemble de verbes utilisés par un formulaire. Dans la structure **SMAPIVerbArray** renvoyée dans le paramètre _ppMAPIVerbArray_ , les verbes sont renvoyés par ordre de numéro d’index ; L’index de chaque verbe se trouve dans son **membre lVerb** . Les applications clientes peuvent utiliser le tableau de verbes pour créer dynamiquement des menus, masquer ou afficher des boutons, etc. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI utilise la méthode **IMAPIFormInfo::CalcVerbSet** lors de l’écriture de la sortie de débogage pour les objets d’informations de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

