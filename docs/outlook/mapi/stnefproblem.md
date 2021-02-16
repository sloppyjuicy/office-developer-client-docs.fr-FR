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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435179"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un problème de traitement de propriété ou d’attribut qui s’est produit lors du codage ou du décodage d’un flux TNEF (Transport Neutral Encapsulation Format).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Tnef.h  <br/> |
   
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
  
> Type de traitement au cours duquel le problème s’est produit. Si le problème s’est produit pendant le traitement des messages, le membre **ulComponent** est définie sur zéro. Si le problème s’est produit lors du traitement des pièces jointes, **ulComponent** est égal à la valeur de la pièce jointe **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
    
 **ulAttribute**
  
> Attribut associé à la propriété indiquée par le membre **ulPropTag** ou, lorsque le problème de traitement TNEF se produit lors du décodage d’un bloc d’encapsulation, l’une des valeurs suivantes : 
    
 _attMAPIProps_
  
> Niveau du message
    
 _attAttachment_
  
> Niveau de pièce jointe
    
 **ulPropTag**
  
> Balise de propriété de la propriété à l’origine du problème de traitement TNEF, sauf lorsque le problème se produit lors du décodage d’un bloc d’encapsulation, auquel cas **ulPropTag** est définie sur zéro. 
    
 **scode**
  
> Valeur d’erreur indiquant le problème rencontré lors du traitement.
    
## <a name="remarks"></a>Remarques

Si une structure **STnefProblem** n’est pas générée pendant le traitement d’un attribut ou d’une propriété, l’application peut continuer en présumant que le traitement de cet attribut ou propriété a réussi. La seule exception se produit lorsque le problème survient lors du décodage d’un bloc d’encapsulation. Dans ce cas, le décodage du composant correspondant au bloc est arrêté et le décodage se poursuit dans un autre composant. 
  
## <a name="see-also"></a>Voir aussi



[STnefProblemArray](stnefproblemarray.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Structures MAPI](mapi-structures.md)

