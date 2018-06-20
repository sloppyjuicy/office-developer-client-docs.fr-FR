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
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787281"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de structures **STnefProblem** décrivant une ou plusieurs des problèmes qui se sont produites pendant le codage de traitement ou de décodage d’un flux de Transport Neutral Encapsulation Format (TNEF). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Membres

 **cProblem**
  
> Nombre d’éléments dans le tableau spécifié dans le membre **aProblem** . 
    
 **aProblem**
  
> Tableau de structures [STnefProblem](stnefproblem.md) . Chaque structure contient des informations sur une propriété ou d’un problème de traitement des attributs. 
    
## <a name="remarks"></a>Remarques

Si un problème survient au cours d’attribut ou de traitement de la propriété, un paramètre de sortie dans la méthode [ITnef::ExtractProps](itnef-extractprops.md) et la méthode de [ITnef::Finish](itnef-finish.md) recevoir un pointeur vers une structure **STnefProblemArray** et le **ExtractProps **et **Terminer** chaque renvoient la valeur MAPI_W_ERRORS_RETURNED. Cette valeur d’erreur indique qu’un problème s’est produit lors du traitement et une structure **STnefProblemArray** a été générée. 
  
Si une structure **STnefProblem** n’est pas générée lors du traitement d’un attribut ou une propriété, l’application cliente peut continuer en supposant que le traitement de cet attribut ou une propriété a réussi. La seule exception se produit lorsque le problème est survenu lors de décodage d’un bloc d’encapsulation. Si l’erreur s’est produite pendant cette décodage, MAPI_E_UNABLE_TO_COMPLETE peut être retourné en tant que le [SCODE](scode.md) dans la structure. Dans ce cas, le décodage du composant correspondant au bloc est arrêté et de décodage se poursuit dans un autre composant. 
  
## <a name="see-also"></a>Voir aussi



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Structures MAPI](mapi-structures.md)

