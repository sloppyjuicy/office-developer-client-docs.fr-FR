---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575328"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient des informations sur un problème de traitement de l’attribut ou propriété qui s’est produite pendant le codage ou de décodage d’un flux de Transport Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Members

 **ulComponent**
  
> Le type de traitement au cours de laquelle le problème est survenu. Si le problème est survenu lors du traitement des messages, le membre **ulComponent** est défini sur zéro. Si le problème s’est produite pendant le traitement des pièces jointes, **ulComponent** est égale à la valeur **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe correspondante.
    
 **ulAttribute**
  
> Attribut associé à la propriété indiquée par le membre **ulPropTag** ou lorsque le problème de traitement TNEF se produit quand une encapsulation de décodage bloquer, une des valeurs suivantes : 
    
 _attMAPIProps_
  
> Niveau de message
    
 _attAttachment_
  
> Au niveau de la pièce jointe
    
 **ulPropTag**
  
> Balise de propriété de la propriété qui a provoqué le problème de traitement TNEF, sauf lorsque le problème se produit lors du décodage d’un bloc d’encapsulation, dans lequel cas **ulPropTag** est définie sur zéro. 
    
 **SCODE**
  
> Valeur d’erreur indiquant le problème rencontré lors du traitement.
    
## <a name="remarks"></a>Remarques

Si une structure **STnefProblem** n’est pas générée lors du traitement d’un attribut ou une propriété, l’application peut poursuivre en supposant que le traitement de cet attribut ou une propriété a réussi. La seule exception se produit lorsque le problème est survenu lors de décodage d’un bloc d’encapsulation. Dans ce cas, le décodage du composant correspondant au bloc est arrêté et de décodage se poursuit dans un autre composant. 
  
## <a name="see-also"></a>Voir aussi



[STnefProblemArray](stnefproblemarray.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Structures MAPI](mapi-structures.md)

