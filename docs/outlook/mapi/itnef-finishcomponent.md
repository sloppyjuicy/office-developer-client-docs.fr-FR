---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0242015680f11e5be6ae8ea9987e5778dc7cdf05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594361"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Traite des composants individuels à partir d’un message à la fois dans un flux de Transport-Neutral Encapsulation Format (TNEF).
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le composant sera terminé. Doit avoir une ou l’autre des indicateurs suivants :
    
TNEF_COMPONENT_ATTACHMENT 
  
> Traitement sera terminé pour un objet attachment ; le paramètre _ulComponentID_ contient la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe. 
    
TNEF_COMPONENT_MESSAGE 
  
> Traitement sera terminé pour un objet de message. 
    
 _ulComponentID_
  
> [in] 0 pour indiquer le traitement d’un message, ou de la propriété **PR_ATTACH_NUM** d’une pièce jointe à traiter. Si l’indicateur TNEF_COMPONENT_MESSAGE est défini dans le paramètre _ulFlags_ , _ulComponentID_ doit être 0. 
    
 _lpCustomPropList_
  
> [in] Un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient des balises de propriété qui identifient les propriétés passé dans le paramètre _lpCustomProps_ . Il doit être une correspondance entre chaque valeur de la propriété dans _lpCustomProps_ et une balise de propriété dans le paramètre _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) qui contienne les valeurs de propriété pour les propriétés à coder. 
    
 _lpPropList_
  
> [in] Pointeur vers une structure **SPropTagArray** qui contient des balises de propriété pour les propriétés à coder. 
    
 _lppProblems_
  
> [out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas échéant, ont été pas codées correctement. Si NULL est indiqué dans le paramètre _lppProblems_ , aucun tableau de problème de propriété n’est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs, les fournisseurs de banque de message et passerelles appel la méthode **ITnef::FinishComponent** pour effectuer le traitement d’un composant, un message ou une pièce jointe TNEF telle qu’indiquée par l’indicateur défini dans le paramètre _ulFlags_ de transport. 
  
Pour le traitement du composant soit activé, le fournisseur ou la passerelle appelant passez l’indicateur TNEF_COMPONENT_ENCODING _ulFlags_ pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) qui ouvre l’objet pour la réception de codage. 
  
Passage de valeurs dans les paramètres _lpCustomPropList_ et _lpCustomProps_ exécute le composant codage équivalentes à celles effectuées par la méthode [ITnef::SetProps](itnef-setprops.md) . Passage d’une valeur dans le paramètre _lpPropList_ effectue composant codage équivalent effectuée par la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE défini dans _ulFlags_. Transmission de ces valeurs permet d’exécuter les codages avec un seul appel au lieu de plusieurs appels.
  
L’implémentation TNEF signale des problèmes de codage TNEF flux sans interrompre le processus **FinishComponent** . La structure **STnefProblemArray** retournée dans _lppProblems_ indique les attributs TNEF ou des propriétés MAPI, le cas échéant, pas peuvent être traitées. La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indiquant le problème spécifique. Le fournisseur ou la passerelle peut travailler sur l’hypothèse que toutes les propriétés ou les attributs pour lesquels **FinishComponent** ne renvoie pas un rapport de problème ont été correctement traités. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux de problème, il peut passer NULL dans _lppProblems_; Dans ce cas, aucun tableau de problème n’est renvoyé.
  
La valeur renvoyée dans _lppProblems_ est valide uniquement si l’appel renvoie S_OK. Lorsque S_OK est retourné, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure [STnefProblemArray](stnefproblemarray.md) . Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie, et la passerelle ou le fournisseur appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l’appel, la passerelle ou le fournisseur appelant doit libérer la mémoire pour le **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

