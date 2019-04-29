---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407500"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait les propriétés d'une encapsulation TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont les propriétés sont décodées. Les indicateurs suivants peuvent être définis:
    
TNEF_PROP_EXCLUDE 
  
> Décode toutes les propriétés non spécifiées dans le paramètre _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Décode toutes les propriétés spécifiées dans _lpPropList_.
    
 _lpPropList_
  
> dans Pointeur vers la liste des propriétés à inclure dans l'opération de décodage ou à exclure de celle-ci.
    
 _lpProblems_
  
> remarquer Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas échéant, qui n'ont pas été codées correctement. Si NULL est passé dans le paramètre _lpProblems_ , aucun tableau de problèmes de propriété n'est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_CORRUPT_DATA 
  
> Les données en cours de décodage dans un flux sont endommagées.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: ExtractProps** pour extraire (c'est-à-dire décoder) les propriétés de l'encapsulation d'un message ou d'une pièce jointe qui a été transmise à la fonction [OpenTnefStream](opentnefstream.md) . Le fournisseur ou la passerelle appelant peut spécifier une liste de propriétés à décoder. Les fournisseurs et les passerelles peuvent également utiliser **ExtractProps** pour fournir des informations sur toute gestion spéciale des pièces jointes. 
  
 **ExtractProps** remplit le message d'origine transmis à **OpenTnefStream** avec les propriétés décodées. Les appels **ExtractProps** suivants renvoient au message et extraient la nouvelle liste de propriétés. 
  
Contrairement à la méthode [ITnef:: AddProps](itnef-addprops.md) , qui met en file d'attente les actions demandées jusqu'à ce que la méthode **ITnef:: Finish** soit appelée, la méthode **ExtractProps** décode les propriétés encapsulées immédiatement lorsqu'elle est appelée. Pour cette raison, le message cible pour le décodage d'encapsulation doit être relativement vide. Les propriétés existantes dans le message cible sont remplacées par les propriétés encapsulées. 
  
 **ExtractProps** est pris en charge uniquement pour les objets ouverts avec l'indicateur TNEF_DECODE pour la fonction **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
L'implémentation TNEF signale les problèmes de codage de flux TNEF sans arrêter le processus **ExtractProps** . La structure [STnefProblemArray](stnefproblemarray.md) renvoyée dans _lpProblems_ indique les attributs TNEF ou les propriétés MAPI, le cas échéant, qui n'ont pas pu être traités. La valeur renvoyée dans le membre **SCODE** de l'une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique. Le fournisseur ou la passerelle peut fonctionner en supposant que toutes les propriétés ou tous les attributs pour lesquels **ExtractProps** ne renvoie pas un rapport de problème ont été traités avec succès. 
  
> [!NOTE]
> Si une propriété dans le bloc d'encapsulation MAPI ne peut pas être traitée et que le flux n'est pas fiable pendant le décodage d'un flux TNEF, le décodage du bloc d'encapsulation est arrêté et un problème est signalé. Le tableau des problèmes pour ce type de problème contient 0L pour **** le membre ulPropTag `attMAPIProps` , `attAttachment` ou pour le membre **ulAttribute** , et MAPI_E_UNABLE_TO_COMPLETE pour le membre **SCODE** . Notez que le décodage du flux n'est pas interrompu, uniquement le décodage du bloc d'encapsulation MAPI. Le décodage de flux continue avec le prochain bloc d'attributs. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec les tableaux de problèmes, elle peut transmettre la valeur NULL dans _lppProblems_; dans ce cas, aucun tableau de problèmes n'est renvoyé. 
  
La valeur renvoyée dans _lpProblems_ est valide uniquement si l'appel retourne S_OK. Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray** . Si une erreur se produit lors de l'appel, la structure **STnefProblemArray** n'est pas renseignée et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l'appel, le fournisseur ou la passerelle d'appel doit libérer la mémoire pour la structure **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

