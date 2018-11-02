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
ms.openlocfilehash: 0765e46a6f0545682b16e484d08d296ea13e2136
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571345"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait les propriétés d’une encapsulation TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les propriétés sont décodées. Les indicateurs suivants peuvent être définis :
    
TNEF_PROP_EXCLUDE 
  
> Décode toutes les propriétés non spécifiées dans le paramètre _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Décode toutes les propriétés spécifiées dans _lpPropList_.
    
 _lpPropList_
  
> [in] Pointeur vers la liste des propriétés à inclure ou exclure de l’opération de décodage.
    
 _lpProblems_
  
> [out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas échéant, ont été pas codées correctement. Si NULL est indiqué dans le paramètre _lpProblems_ , aucun tableau de problème de propriété n’est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
MAPI_E_CORRUPT_DATA 
  
> En cours de décodage dans un flux de données sont endommagées.
    
## <a name="remarks"></a>Remarques

Fournisseurs de transport, les fournisseurs de banque de message et passerelles appellent la méthode de **ITnef::ExtractProps** pour extraire (qui est, décoder) propriétés à partir de l’encapsulation d’un message ou d’une pièce jointe qui a été passée à la fonction [OpenTnefStream](opentnefstream.md) . La passerelle ou le fournisseur appelant peut spécifier une liste de propriétés à décoder. Fournisseurs et des passerelles peuvent également utiliser **ExtractProps** pour fournir des informations sur aucun traitement spécial pour les pièces jointes. 
  
 **ExtractProps** remplit le message d’origine est passé en **OpenTnefStream** avec les propriétés décodées. Les appels suivants **ExtractProps** revenir au message et extrayez la nouvelle liste de propriétés. 
  
Contrairement à la méthode [ITnef::AddProps](itnef-addprops.md) , files d’attente demandé actions jusqu'à ce que la méthode **ITnef::Finish** est appelée, la méthode **ExtractProps** décode les propriétés encapsulées immédiatement lorsqu’elle est appelée. Pour cette raison, le message cible de décodage encapsulation doit être relativement vide. Propriétés existantes dans le message cible sont remplacées par les propriétés encapsulées. 
  
 **ExtractProps** est pris en charge uniquement pour les objets qui sont ouverts avec l’indicateur TNEF_DECODE pour la fonction **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
L’implémentation TNEF signale des problèmes de codage TNEF flux sans interrompre le processus **ExtractProps** . La structure [STnefProblemArray](stnefproblemarray.md) retournée dans _lpProblems_ indique les attributs TNEF ou des propriétés MAPI, le cas échéant, pas peuvent être traitées. La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indiquant le problème spécifique. Le fournisseur ou la passerelle peut travailler sur l’hypothèse que toutes les propriétés ou les attributs pour lesquels **ExtractProps** ne renvoie pas un rapport de problème ont été correctement traités. 
  
> [!NOTE]
> Si une propriété dans le bloc d’encapsulation MAPI ne peut pas être traitée et laisse le flux non fiables pendant le décodage d’un flux TNEF, décodage du bloc encapsulation est arrêté et un problème est signalé. Le tableau de problème pour ce type de problème contient 0L du membre **ulPropTag** , `attMAPIProps` ou `attAttachment` pour le membre **ulAttribute** et MAPI_E_UNABLE_TO_COMPLETE du membre **scode** . Notez que le décodage du flux n’est pas interrompu, simplement le décodage du bloc encapsulation MAPI. Le décodage des flux se poursuit avec le bloc d’attributs suivant. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux de problème, il peut passer NULL dans _lppProblems_; Dans ce cas, aucun tableau de problème n’est renvoyé. 
  
La valeur renvoyée dans _lpProblems_ est valide uniquement si l’appel renvoie S_OK. Lorsque S_OK est retourné, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray** . Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas renseignée et la passerelle ou le fournisseur appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l’appel, la passerelle ou le fournisseur appelant doit libérer de la mémoire de la structure **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

