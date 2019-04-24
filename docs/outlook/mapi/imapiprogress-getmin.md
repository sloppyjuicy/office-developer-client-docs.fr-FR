---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331681"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la valeur minimale dans la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) pour laquelle les informations de progression sont affichées. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Paramètres

 _lpulMin_
  
> [out] Pointeur vers le nombre minimal d’éléments dans l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre minimal d’éléments dans l’opération a été récupéré.
    
## <a name="remarks"></a>Remarques

La valeur minimale représente le début de l’opération au format numérique. La valeur peut être une valeur maximale globale, utilisée pour représenter l’étendue de l’intégralité de l’affichage de la progression, ou une valeur locale, utilisée pour représenter uniquement une partie de l’affichage. 
  
La valeur du paramètre d’indicateur permet de déterminer si l’objet de progression considère la valeur minimale comme locale ou globale. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur minimale est globale et sert à calculer la progression pour l’intégralité de l’opération. Si MAPI_TOP_LEVEL n’est pas défini, la valeur minimale est locale, et les fournisseurs l’utilisent en interne afin d’afficher la progression pour les sous-objets de niveau inférieur. Les objets de progression enregistrent la valeur minimale locale uniquement pour la renvoyer à un fournisseur par le biais d’un appel **GetMin**. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Initialisez la valeur minimale sur 1. Les fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode **IMAPIProgress::SetLimits**. Pour plus d’informations sur la méthode d’implémentation de la méthode **GetMin** et des autres méthodes [IMAPIProgress](imapiprogressiunknown.md), reportez-vous à la rubrique [Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::GetMin** afin d’obtenir la valeur minimale pour l’indicateur de progression. Renvoie la valeur 1 sauf si des limites ont précédemment été définies au moyen de l’appel de la méthode **IMAPIProgress::SetLimits**.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

