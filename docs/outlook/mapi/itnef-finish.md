---
title: ITnefFinish
description: ITnefFinish termine le traitement de toutes les opérations TNEF (Encapsulation Format) Transport-Neutral qui sont mises en file d’attente et en attente.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
ms.openlocfilehash: 63d5ef803211fd9851bd9dd953e0f215d4862589
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828079"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Termine le traitement de toutes les opérations TNEF (Transport-Neutral Encapsulation Format) en file d’attente. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpKey_
  
> [out] Pointeur vers la propriété de clé **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe. L’objet d’encapsulation TNEF utilise cette clé pour faire correspondre une pièce jointe à sa balise de placement de pièce jointe dans un message. Cette clé doit être unique à chaque pièce jointe.
    
 _lpProblem_
  
> [out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) retournée. La structure **STnefProblemArray** indique quelles propriétés, le cas échéant, n’ont pas été encodées correctement. Si null est passé dans le paramètre _lpProblem_ , aucun tableau de problèmes de propriété n’est retourné. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et retourné la valeur ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::Finish** pour effectuer l’encodage de toutes les propriétés pour lesquelles l’encodage a été demandé dans les appels aux méthodes [ITnef::AddProps](itnef-addprops.md) et [ITnef::SetProps](itnef-setprops.md) . Si l’objet TNEF a été ouvert avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) , la méthode **Finish** encode les propriétés demandées dans le flux d’encapsulation transmis à cet objet. Si l’objet TNEF a été ouvert avec l’indicateur TNEF_DECODE, la méthode **Finish** décode les propriétés du flux TNEF et les réécrit dans le message auquel elles appartiennent. 
  
Après l’appel **finish** , le pointeur vers le flux d’encapsulation pointe vers la fin des données TNEF. Si le fournisseur ou la passerelle doit utiliser les données de flux TNEF après l’appel **de fin** , il doit réinitialiser le pointeur de flux au début des données de flux TNEF. 
  
L’implémentation TNEF signale des problèmes d’encodage de flux TNEF sans arrêter le processus **de fin** . La structure [STnefProblemArray](stnefproblemarray.md) retournée dans le paramètre _lpProblem_ indique quels attributs TNEF ou propriétés MAPI, le cas échéant, n’ont pas pu être traités. La valeur retournée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique. Le fournisseur ou la passerelle peut fonctionner en partant du principe que toutes les propriétés ou attributs pour lesquels **Finish** ne retourne pas de rapport de problème ont été traités avec succès. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux de problèmes, il peut passer NULL dans  _lpProblem_ ; Dans ce cas, aucun tableau de problèmes n’est retourné. 
  
La valeur retournée dans  _lpProblem_ est valide uniquement si l’appel retourne S_OK. Lorsque S_OK est retourné, le fournisseur ou la passerelle doit vérifier les valeurs retournées dans la structure **STnefProblemArray** . Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l’appel, le fournisseur ou la passerelle appelant doit libérer la mémoire de **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la méthode **ITnef::Finish** pour terminer le traitement du nouveau flux TNEF. |
   
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber, propriété canonique](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

