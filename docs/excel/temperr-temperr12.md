---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- function [excel 2007],TempErr12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
ms.openlocfilehash: 0a335f5a1d4044b44fca7e992052709b915a93d5
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198442"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework qui crée une **xlOPER** /  **XLOPER12** temporaire contenant une erreur Microsoft Excel feuille de calcul. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Paramètres

 _err_
  
Code d’erreur souhaité, ou son équivalent numérique littéral, comme indiqué dans le tableau suivant.
  
|**Erreur**|**Code d’erreur défini dans XLCALL. H**|**Équivalent décimal**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7   <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15   <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME ?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

Renvoie un **xltypeBool** contenant le code d’erreur passé. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction TempErr12** pour renvoyer une #VALUE! erreur à Excel. 
  
> [!NOTE]
> La fonction de bibliothèque **Framework TempErr12** alloue de la mémoire à partir d’une mémoire tampon interne, qui est normalement libérée lorsque la fonction **Framework Excel12f** est appelée. Si cet exemple de fonction est appelé à plusieurs reprises sans **qu’Excel12f** soit appelé, une fuite de mémoire se produit. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

