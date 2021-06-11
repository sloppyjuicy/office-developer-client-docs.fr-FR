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
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416439"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Traite les composants individuels d’un message un par un dans Transport-Neutral flux TNEF (Encapsulation Format).
  
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le composant à terminer. L’un ou l’autre des indicateurs suivants doit être définie :
    
TNEF_COMPONENT_ATTACHMENT 
  
> Le traitement sera terminé pour un objet pièce jointe . le  _paramètre ulComponentID_ contient la **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe. 
    
TNEF_COMPONENT_MESSAGE 
  
> Le traitement est terminé pour un objet message. 
    
 _ulComponentID_
  
> [in] 0 pour indiquer le traitement d’un message ou la propriété **PR_ATTACH_NUM** d’une pièce jointe à traiter. Si l TNEF_COMPONENT_MESSAGE est définie dans le paramètre  _ulFlags,_  _ulComponentID_ doit être 0. 
    
 _lpCustomPropList_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient des balises de propriété qui identifient les propriétés transmises dans le paramètre _lpCustomProps._ Il doit y avoir une correspondance un-à-un entre chaque valeur de propriété dans _lpCustomProps_ et une balise de propriété dans le paramètre _lpCustomPropList._ 
    
 _lpCustomProps_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) qui contient les valeurs des propriétés à coder. 
    
 _lpPropList_
  
> [in] Pointeur vers une structure **SPropTagArray** qui contient des balises de propriété pour les propriétés à encoder. 
    
 _lppProblems_
  
> [out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas contraire, qui n’ont pas été correctement codées. Si NULL est transmis dans le  _paramètre lppProblems,_ aucun tableau de problèmes de propriété n’est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::FinishComponent** pour effectuer un traitement TNEF pour un composant, soit un message, soit une pièce jointe, comme indiqué par l’indicateur définie dans le paramètre _ulFlags._ 
  
Pour que le traitement des composants soit activé, le fournisseur ou la passerelle appelant passe l’indicateur TNEF_COMPONENT_ENCODING dans  _ulFlags_ pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) qui a ouvert l’objet pour recevoir le codage. 
  
La transmission de valeurs dans les paramètres _lpCustomPropList_ et _lpCustomProps_ effectue un codage de composant équivalent à celui effectué par la méthode [ITnef::SetProps.](itnef-setprops.md) La transmission d’une valeur dans le paramètre  _lpPropList_ effectue un codage de composant équivalent à celui effectué par la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE définie dans  _ulFlags_. La transmission de ces valeurs vous permet d’effectuer des codages avec un seul appel au lieu de plusieurs appels.
  
L’implémentation TNEF signale des problèmes de codage de flux TNEF sans arrêter **le processus FinishComponent.** La structure **STnefProblemArray** renvoyée dans  _lppProblems_ indique quels attributs TNEF ou propriétés MAPI, le cas contraire, n’ont pas pu être traitées. La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique. Le fournisseur ou la passerelle peut fonctionner sur l’hypothèse que toutes les propriétés ou attributs pour lesquels **FinishComponent** ne retourne pas de rapport de problème ont été correctement traitées. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux à problème, il peut transmettre null dans  _lppProblems_; dans ce cas, aucun tableau de problèmes n’est renvoyé.
  
La valeur renvoyée dans  _lppProblems n’est_ valide que si l’appel S_OK. Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure [STnefProblemArray.](stnefproblemarray.md) Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit sur l’appel, le fournisseur ou la passerelle appelant doit libérer la mémoire de **l’objet STnefProblemArray** en appelant la fonction [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

