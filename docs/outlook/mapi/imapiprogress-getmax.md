---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436201"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le nombre maximal d’éléments dans l’opération pour lesquels les informations de progression sont affichées.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parameters

 _lpulMax_
  
> [out] Pointeur vers le nombre maximal d’éléments dans l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre maximal d’éléments de l’opération a été récupéré.
    
## <a name="remarks"></a>Remarques

La valeur maximale représente la fin de l’opération sous forme numérique. La valeur peut être une valeur maximale globale, utilisée pour représenter l’étendue de l’intégralité de l’affichage de la progression, ou une valeur locale, utilisée pour représenter uniquement une partie de l’affichage. 
  
La valeur du paramètre d’indicateur a une incidence sur le fait que l’objet de progression comprenne la valeur maximale à être locale ou globale. Lorsque l MAPI_TOP_LEVEL est définie, la valeur maximale est considérée comme globale et est utilisée pour calculer la progression de l’ensemble de l’opération. Lorsque MAPI_TOP_LEVEL n’est pas définie, la valeur maximale est considérée comme locale et les fournisseurs l’utilisent en interne pour afficher la progression des sous-objets de niveau inférieur. Les objets de progression enregistrent la valeur maximale locale uniquement pour la renvoyer à un fournisseur via un **appel GetMax.** 
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Initialise la valeur maximale à 1 000. Les fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Pour plus d’informations sur l’implémentation de **GetMax** et des autres méthodes [IMAPIProgress,](imapiprogressiunknown.md) voir [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI utilise la **méthode IMAPIProgress::GetMax** pour obtenir la valeur maximale de l’objet de progression. Renvoie 1000, sauf si des limites ont été précédemment définies avec la méthode **IMAPIProgress::SetLimits.**  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

