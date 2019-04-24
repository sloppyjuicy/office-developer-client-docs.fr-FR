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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278885"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Traite les composants individuels d'un message un à la fois dans un flux TNEF (Transport-Neutral Encapsulation Format).
  
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

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le composant qui sera terminé. L'un des indicateurs suivants doit être défini:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Le traitement sera terminé pour un objet Attachment; le paramètre _ulComponentID_ contient la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe. 
    
TNEF_COMPONENT_MESSAGE 
  
> Le traitement sera terminé pour un objet message. 
    
 _ulComponentID_
  
> [in] 0 pour indiquer le traitement d'un message ou la propriété **PR_ATTACH_NUM** d'une pièce jointe à traiter. Si l'indicateur TNEF_COMPONENT_MESSAGE est défini dans le paramètre _ulFlags_ , _ulComponentID_ doit être égal à 0. 
    
 _lpCustomPropList_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient les balises de propriété qui identifient les propriétés transmises dans le paramètre _lpCustomProps_ . Il doit y avoir une correspondance un-à-un entre chaque valeur de propriété dans _lpCustomProps_ et une balise de propriété dans le paramètre _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> dans Pointeur vers une structure [SPropValue](spropvalue.md) qui contient des valeurs de propriété pour les propriétés à encoder. 
    
 _lpPropList_
  
> dans Pointeur vers une structure **SPropTagArray** qui contient les balises de propriété pour les propriétés à encoder. 
    
 _lppProblems_
  
> remarquer Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas échéant, qui n'ont pas été codées correctement. Si NULL est passé dans le paramètre _lppProblems_ , aucun tableau de problèmes de propriété n'est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: FinishComponent** pour effectuer le traitement TNEF pour un composant, qu'il s'agisse d'un message ou d'une pièce jointe, comme indiqué par l'indicateur défini dans le paramètre _ulFlags_ . 
  
Pour que le traitement du composant soit activé, le fournisseur d'appels ou la passerelle transmet l'indicateur TNEF_COMPONENT_ENCODING dans _ulFlags_ pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) qui a ouvert l'objet pour recevoir le codage. 
  
Le passage de valeurs dans les paramètres _lpCustomPropList_ et _lpCustomProps_ effectue un codage des composants équivalent à celui effectué par la méthode [ITnef:: SetProps](itnef-setprops.md) . Le passage d'une valeur dans le paramètre _lpPropList_ effectue un codage de composant équivalent à celui effectué par la méthode [ITnef:: AddProps](itnef-addprops.md) avec l'indicateur TNEF_PROP_INCLUDE défini dans _ulFlags_. La transmission de ces valeurs vous permet d'effectuer des encodages avec un seul appel au lieu de plusieurs appels.
  
L'implémentation TNEF signale les problèmes de codage de flux TNEF sans arrêter le processus **FinishComponent** . La structure **STnefProblemArray** renvoyée dans _lppProblems_ indique les attributs TNEF ou les propriétés MAPI, le cas échéant, qui n'ont pas pu être traités. La valeur renvoyée dans le membre **SCODE** de l'une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique. Le fournisseur ou la passerelle peut fonctionner en supposant que toutes les propriétés ou tous les attributs pour lesquels **FinishComponent** ne renvoie pas un rapport de problème ont été traités avec succès. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec les tableaux de problèmes, elle peut transmettre la valeur NULL dans _lppProblems_; dans ce cas, aucun tableau de problèmes n'est renvoyé.
  
La valeur renvoyée dans _lppProblems_ est valide uniquement si l'appel retourne S_OK. Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure [STnefProblemArray](stnefproblemarray.md) . Si une erreur se produit lors de l'appel, la structure **STnefProblemArray** n'est pas renseignée et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l'appel, le fournisseur ou la passerelle d'appel doit libérer la mémoire pour l' **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

