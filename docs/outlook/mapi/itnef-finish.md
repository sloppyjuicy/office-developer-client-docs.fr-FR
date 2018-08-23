---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583763"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fin de traitement de toutes les opérations de Transport-Neutral Encapsulation Format (TNEF) qui sont en file d’attente et en attente. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpKey_
  
> [out] Pointeur vers la propriété clé **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe. L’objet de l’encapsulation TNEF utilise cette clé pour la correspondance de pièce jointe à une balise de positionnement de pièce jointe dans un message. Cette clé doit être unique pour chaque pièce jointe.
    
 _lpProblem_
  
> [out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas échéant, ont été pas codées correctement. Si NULL est indiqué dans le paramètre _lpProblem_ , aucun tableau de problème de propriété n’est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs, les fournisseurs de banque de message et appel passerelles la méthode **ITnef::Finish** pour effectuer le codage de toutes les propriétés pour le codage a été demandée dans les appels aux méthodes [ITnef::AddProps](itnef-addprops.md) et [ITnef::SetProps](itnef-setprops.md) de transport. Si l’objet TNEF a été ouvert avec l’indicateur TNEF_ENCODE pour la [OpenTnefStream](opentnefstream.md) ou la fonction [OpenTnefStreamEx](opentnefstreamex.md) , la méthode **fin** encode les propriétés demandées dans le flux d’encapsulation transmis à cet objet. Si l’objet TNEF a été ouvert avec l’indicateur TNEF_DECODE, la méthode **fin** décode les propriétés à partir du flux TNEF et les écrit dans le message qu'auxquels ils appartiennent. 
  
Après l’appel **de fin** , le pointeur vers le flux d’encapsulation pointe vers la fin des données TNEF. Si le fournisseur ou la passerelle doit utiliser les données du flux TNEF après la **fin** de l’appel, il doit réinitialiser le pointeur du flux au début des données stream TNEF. 
  
L’implémentation TNEF signale des problèmes de codage TNEF flux sans interrompre le processus **de fin** . La structure [STnefProblemArray](stnefproblemarray.md) retournée dans le paramètre _lpProblem_ indique les attributs TNEF ou des propriétés MAPI, le cas échéant, pas peuvent être traitées. La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indiquant le problème spécifique. Le fournisseur ou la passerelle peut travailler sur l’hypothèse que toutes les propriétés ou les attributs pour lesquels **fin** ne retourne un rapport de problème ont été correctement traités. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux de problème, il peut passer NULL dans _lpProblem_; Dans ce cas, aucun tableau de problème n’est renvoyé. 
  
La valeur renvoyée dans _lpProblem_ est valide uniquement si l’appel renvoie S_OK. Lorsque S_OK est retourné, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray** . Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas renseignée et la passerelle ou le fournisseur appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l’appel, la passerelle ou le fournisseur appelant doit libérer la mémoire pour le **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la méthode **ITnef::Finish** pour terminer le traitement du nouveau flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

