---
title: IMAPIFormInfoCalcFormPropSet
description: Décrit la syntaxe, les paramètres et la valeur de retour pour IMAPIFormInfoCalcFormPropSet, qui retourne un pointeur vers l’ensemble complet de propriétés qu’un formulaire utilise.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
ms.openlocfilehash: da7081c1833a928b3fb902535c2b289a0e86b522
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816345"
---
# <a name="imapiforminfocalcformpropset"></a>IMAPIFormInfo::CalcFormPropSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers l’ensemble complet des propriétés utilisées par un formulaire.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type de chaînes retournées. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
 _ppFormPropArray_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) retournée. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI utilise la méthode **IMAPIFormInfo::CalcFormPropSet** lors de l’écriture d’une sortie de débogage pour les objets d’informations de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

