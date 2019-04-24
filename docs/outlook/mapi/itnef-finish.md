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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348586"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Termine le traitement de toutes les opérations TNEF (Transport-Neutral Encapsulation Format) mises en file d'attente et en attente. 
  
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
  
> remarquer Pointeur vers la propriété de clé **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d'une pièce jointe. L'objet d'encapsulation TNEF utilise cette clé pour faire correspondre une pièce jointe à sa balise de placement de pièce jointe dans un message. Cette clé doit être unique pour chaque pièce jointe.
    
 _lpProblem_
  
> remarquer Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas échéant, qui n'ont pas été codées correctement. Si NULL est passé dans le paramètre _lpProblem_ , aucun tableau de problèmes de propriété n'est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: Finish** pour effectuer le codage de toutes les propriétés pour lesquelles le codage a été demandé dans les appels aux méthodes [ITnef:: AddProps](itnef-addprops.md) et [ITnef:: SetProps](itnef-setprops.md) . Si l'objet TNEF a été ouvert avec l'indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) , la méthode **Finish** encode les propriétés demandées dans le flux d'encapsulation transmis à cet objet. Si l'objet TNEF a été ouvert avec l'indicateur TNEF_DECODE, la méthode **Finish** décode les propriétés du flux TNEF et les réécrit dans le message auquel elles appartiennent. 
  
Après l'appel de **fin** , le pointeur vers le flux d'encapsulation pointe vers la fin des données TNEF. Si le fournisseur ou la passerelle doit utiliser les données de flux TNEF après l'appel de **fin** , il doit réinitialiser le pointeur de flux au début des données de flux TNEF. 
  
L'implémentation TNEF signale les problèmes de codage de flux TNEF sans arrêter le processus de **fin** . La structure [STnefProblemArray](stnefproblemarray.md) renvoyée dans le paramètre _lpProblem_ indique les attributs TNEF ou les propriétés MAPI, le cas échéant, qui n'ont pas pu être traités. La valeur renvoyée dans le membre **SCODE** de l'une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique. Le fournisseur ou la passerelle peut fonctionner en supposant que toutes les propriétés ou tous les attributs pour lesquels la **fin** ne renvoie pas de rapport de problème ont été traités. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec les tableaux de problèmes, elle peut transmettre la valeur NULL dans _lpProblem_; dans ce cas, aucun tableau de problèmes n'est renvoyé. 
  
La valeur renvoyée dans _lpProblem_ est valide uniquement si l'appel retourne S_OK. Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray** . Si une erreur se produit lors de l'appel, la structure **STnefProblemArray** n'est pas renseignée et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l'appel, le fournisseur ou la passerelle d'appel doit libérer la mémoire pour l' **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File. cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la méthode **ITnef:: Finish** pour terminer le traitement du nouveau flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

