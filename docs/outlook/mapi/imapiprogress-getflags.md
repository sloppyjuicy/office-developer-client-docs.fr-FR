---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423642"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les paramètres d'indicateur à partir de l'objet de progression pour le niveau d'opération sur lequel les informations de progression sont calculées.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> remarquer Masque de des indicateurs qui contrôle le niveau d'opération sur lequel les informations de progression sont calculées. L'indicateur suivant peut être renvoyé:
    
MAPI_TOP_LEVEL 
  
> La progression est calculée pour l'objet de niveau supérieur, l'objet qui est appelé par le client pour commencer l'opération. Par exemple, l'objet de niveau supérieur dans une opération de copie de dossier est le dossier en cours de copie. Lorsque MAPI_TOP_LEVEL n'est pas défini, Progress est calculé pour un objet de niveau inférieur ou un sous-objet. Dans l'opération de copie de dossier, un objet de niveau inférieur est l'un des sous-dossiers dans le dossier en cours de copie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La valeur flags a été renvoyée.
    
## <a name="remarks"></a>Remarques

MAPI permet aux fournisseurs de services de différencier les objets de niveau supérieur et les sous-objets à l'aide de l'indicateur MAPI_TOP_LEVEL afin que tous les objets impliqués dans une opération puissent utiliser la même implémentation [méthode imapiprogress](imapiprogressiunknown.md) pour afficher la progression. Ainsi, l'indicateur s'affiche en douceur dans une seule direction positive. La définition de l'indicateur MAPI_TOP_LEVEL détermine la façon dont les fournisseurs de services définissent les autres paramètres dans les appels ultérieurs à l'objet Progress. 
  
La valeur renvoyée par **GetFlags** est initialement définie par l'implémenteur et par la suite par le fournisseur de services par le biais d'un appel à la méthode [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Initialisez toujours l'indicateur sur MAPI_TOP_LEVEL, puis faites en sorte que les fournisseurs de services l'efface lorsque cela est nécessaire. Les fournisseurs de services peuvent effacer et réinitialiser l'indicateur en appelant la méthode **méthode imapiprogress:: SetLimits** . Pour plus d'informations sur la façon d'implémenter **GetFlags** et les autres méthodes **méthode imapiprogress** , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous affichez un indicateur de progression, appelez d'abord un appel à **méthode imapiprogress:: GetFlags**. La valeur renvoyée doit être MAPI_TOP_LEVEL, car toutes les implémentations initialisent le contenu du paramètre _lpulFlags_ à cette valeur. Pour plus d'informations sur la séquence d'appels à un objet Progress, voir [afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: GetFlags  <br/> |MFCMAPI utilise la méthode **méthode imapiprogress:: GetFlags** pour déterminer les indicateurs définis. Renvoie MAPI_TOP_LEVEL sauf si les indicateurs ont été définis à l'aide de la méthode **méthode imapiprogress:: SetLimits** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

