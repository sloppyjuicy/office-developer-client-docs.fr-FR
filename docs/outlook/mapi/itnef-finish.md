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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435676"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Termine le traitement de toutes les Transport-Neutral de format d’encapsulation (TNEF) qui sont en file d’attente. 
  
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
  
> [out] Pointeur vers la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe. L’objet d’encapsulation TNEF utilise cette clé pour faire correspondre une pièce jointe à sa balise de placement des pièces jointes dans un message. Cette clé doit être unique pour chaque pièce jointe.
    
 _lpProblem_
  
> [out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée. La structure **STnefProblemArray** indique les propriétés, le cas contraire, qui n’ont pas été correctement codées. Si NULL est transmis dans le  _paramètre lpProblem,_ aucun tableau de problèmes de propriété n’est renvoyé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::Finish** pour effectuer le codage de toutes les propriétés pour lesquelles le codage a été demandé dans les appels aux méthodes [ITnef::AddProps](itnef-addprops.md) et [ITnef::SetProps.](itnef-setprops.md) Si l’objet TNEF a été ouvert avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx,](opentnefstreamex.md) la méthode **Finish** code les propriétés demandées dans le flux d’encapsulation transmis à cet objet. Si l’objet TNEF a été ouvert avec l’indicateur TNEF_DECODE, la méthode **Finish** décode les propriétés du flux TNEF et les écrit dans le message à qui ils appartiennent. 
  
Après **l’appel Terminer,** le pointeur vers le flux d’encapsulation pointe vers la fin des données TNEF. Si le fournisseur ou la passerelle doit utiliser  les données de flux TNEF après l’appel de fin, il doit réinitialiser le pointeur de flux au début des données de flux TNEF. 
  
L’implémentation TNEF signale des problèmes de codage de flux TNEF sans arrêter **le processus Finish.** La structure [STnefProblemArray](stnefproblemarray.md) renvoyée dans le paramètre  _lpProblem_ indique quels attributs TNEF ou propriétés MAPI, le cas contraire, n’ont pas pu être traitées. La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique. Le fournisseur ou la passerelle peut fonctionner sur l’hypothèse que toutes les propriétés ou attributs pour lesquels **Finish** ne retourne pas de rapport de problème ont été correctement traitées. 
  
Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux à problème, il peut transmettre null dans  _lpProblem_; dans ce cas, aucun tableau de problèmes n’est renvoyé. 
  
La valeur renvoyée dans  _lpProblem_ n’est valide que si l’appel S_OK. Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray.** Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure. Si aucune erreur ne se produit lors de l’appel, le fournisseur ou la passerelle appelant doit libérer la mémoire de **l’objet STnefProblemArray** en appelant la fonction [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la **méthode ITnef::Finish** pour terminer le traitement du nouveau flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

