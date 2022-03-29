---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: Contient des informations sur un problème de traitement de propriété ou d’attribut qui s’est produit lors du codage ou du décodage d’un flux TNEF.
ms.openlocfilehash: bf88b1ccd9bcff4dce6e0a8ac8719c1d133afadb
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455012"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un problème de traitement de propriété ou d’attribut qui s’est produit lors du codage ou du décodage d’un flux TNEF (Transport Neutral Encapsulation Format).
  
|Propriété |Valeur |
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
  
> Type de traitement au cours duquel le problème s’est produit. Si le problème s’est produit pendant le traitement des messages, le membre **ulComponent** est définie sur zéro. Si le problème s’est produit lors du traitement des pièces jointes, **ulComponent** est égal à la valeur **PR_ATTACH_NUM (**[PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe correspondante.
    
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

