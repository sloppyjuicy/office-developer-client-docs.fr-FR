---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336497"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures **STnefProblem** décrivant un ou plusieurs problèmes de traitement qui se sont produits pendant le codage ou le décodage d'un flux TNEF (Transport Neutral Encapsulation Format). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF. h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **cProblem**
  
> Nombre d'éléments dans le tableau spécifié dans le membre **aProblem** . 
    
 **aProblem**
  
> Tableau de structures [STnefProblem](stnefproblem.md) . Chaque structure contient des informations sur un problème de traitement de propriété ou d'attribut. 
    
## <a name="remarks"></a>Remarques

Si un problème se produit pendant le traitement des attributs ou des propriétés, un paramètre de sortie dans la méthode [ITnef:: ExtractProps](itnef-extractprops.md) et dans la méthode [ITnef:: Finish](itnef-finish.md) reçoit un pointeur vers une structure **STnefProblemArray** et **ExtractProps **et **finally** renvoient la valeur MAPI_W_ERRORS_RETURNED. Cette valeur d'erreur indique qu'un problème est survenu pendant le traitement et qu'une structure **STnefProblemArray** a été générée. 
  
Si une structure **STnefProblem** n'est pas générée pendant le traitement d'un attribut ou d'une propriété, l'application cliente peut continuer en supposant que le traitement de cet attribut ou de cette propriété a réussi. La seule exception se produit lors du décodage d'un bloc d'encapsulation. Si l'erreur s'est produite pendant ce décodage, MAPI_E_UNABLE_TO_COMPLETE peut être renvoyé comme [SCODE](scode.md) dans la structure. Dans ce cas, le décodage du composant correspondant au bloc est arrêté et le décodage se poursuit dans un autre composant. 
  
## <a name="see-also"></a>Voir aussi



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Structures MAPI](mapi-structures.md)

