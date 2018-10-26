---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db3cc987b20a76116f2591485f57afae017d3e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567712"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers l’ensemble complet des verbes qui utilise un formulaire.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _ppMAPIVerbArray_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIVerbArray](smapiverbarray.md) retournée qui contient les verbes du formulaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **IMAPIFormInfo::CalcVerbSet** pour obtenir un pointeur vers l’ensemble de verbes utilisés par un formulaire. Dans la structure **SMAPIVerbArray** retournée dans le paramètre _ppMAPIVerbArray_ , les verbes sont retournés dans l’ordre de numéro d’index ; index de chaque verbe se trouve dans son membre **lVerb** . Applications clientes permet le tableau verbe dynamiquement créer des menus, masquer ou afficher les boutons et ainsi de suite. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI utilise la méthode **IMAPIFormInfo::CalcVerbSet** lors de l’écriture de sortie de débogage pour les objets d’informations de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

