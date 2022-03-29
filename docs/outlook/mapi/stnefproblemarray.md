---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: Contient un tableau de structures STnefProblem décrivant un ou plusieurs problèmes de traitement qui se sont produits lors du codage ou du décodage d’un flux TNEF.
ms.openlocfilehash: 700b822e3c38cbaf41a12aa150bd0bce15ac4b51
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455005"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures **STnefProblem** décrivant un ou plusieurs problèmes de traitement qui se sont produits lors du codage ou du décodage d’un flux TNEF (Transport Neutral Encapsulation Format). 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **cProblem**
  
> Nombre d’éléments dans le tableau spécifié dans le **membre aProblem** . 
    
 **aProblem**
  
> Tableau de structures [STnefProblem](stnefproblem.md) . Chaque structure contient des informations sur un problème de traitement de propriété ou d’attribut. 
    
## <a name="remarks"></a>Remarques

Si un problème se produit lors du traitement des attributs ou des propriétés, un paramètre de sortie dans la méthode [ITnef::ExtractProps](itnef-extractprops.md) et dans la méthode [ITnef::Finish](itnef-finish.md) reçoivent chacun un pointeur vers une structure **STnefProblemArray** et **ExtractProps** et **Finish** retournent chacun la valeur MAPI_W_ERRORS_RETURNED. Cette valeur d’erreur indique qu’un problème s’est produit lors du traitement et qu’une structure **STnefProblemArray** a été générée. 
  
Si une structure **STnefProblem** n’est pas générée pendant le traitement d’un attribut ou d’une propriété, l’application cliente peut continuer en présumant que le traitement de cet attribut ou propriété a réussi. La seule exception se produit lorsque le problème survient lors du décodage d’un bloc d’encapsulation. Si l’erreur s’est produite pendant ce décodage, MAPI_E_UNABLE_TO_COMPLETE peut être renvoyé en tant que [code SCODE](scode.md) dans la structure. Dans ce cas, le décodage du composant correspondant au bloc est arrêté et le décodage se poursuit dans un autre composant. 
  
## <a name="see-also"></a>Voir aussi



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Structures MAPI](mapi-structures.md)

