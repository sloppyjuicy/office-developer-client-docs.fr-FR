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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783880"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**S’applique à**: Outlook 
  
L’indicateur renvoie les paramètres de l’objet de l’avancement du niveau de l’opération sur lequel les informations d’avancement sont calculées.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [out] Masque de bits d’indicateurs qui contrôle le niveau de l’opération sur l’avancement des informations sont calculées. L’indicateur suivantes peut être renvoyées :
    
MAPI_TOP_LEVEL 
  
> Progression est calculée pour l’objet de niveau supérieur, l’objet qui est appelée par le client doit commencer l’opération. Par exemple, l’objet de niveau supérieur dans une opération de copie du dossier est le dossier en cours de copie. Lorsque MAPI_TOP_LEVEL n’est pas défini, l’avancement est calculé pour un objet de niveau inférieur ou sous-objet. Dans l’opération de copie de dossier, un objet de niveau inférieur est un des sous-dossiers dans le dossier en cours de copie.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La valeur flags a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

MAPI permet aux prestataires de faire la distinction entre les objets de niveau supérieur et sous-objets avec l’indicateur MAPI_TOP_LEVEL afin que tous les objets impliquant dans une opération peuvent utiliser la même implémentation [IMAPIProgress](imapiprogressiunknown.md) pour afficher la progression. Cela entraîne l’affichage de l’indicateur en douceur dans un seul sens positif. Si l’indicateur MAPI_TOP_LEVEL est défini détermine comment les fournisseurs de services de définissent les autres paramètres dans les appels suivants à l’objet de l’avancement. 
  
La valeur renvoyée par **GetFlags** est initialement définie par l’implémentation et par la suite par le fournisseur de services via un appel à la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Toujours initialiser l’indicateur MAPI_TOP_LEVEL, puis ils s’appuient sur les fournisseurs de services pour la désactiver le cas échéant. Fournisseurs de services peuvent supprimer et réinitialiser l’indicateur en appelant la méthode **IMAPIProgress::SetLimits** . Pour plus d’informations sur la façon d’implémenter **GetFlags** et les autres méthodes **IMAPIProgress** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque vous affichez un indicateur de progression, appelez votre premier appel un **IMAPIProgress::GetFlags**. La valeur renvoyée doit être MAPI_TOP_LEVEL, car toutes les implémentations initialiser le contenu du paramètre _lpulFlags_ à cette valeur. Pour plus d’informations sur la séquence d’appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::GetFlags** pour déterminer les indicateurs sont définis. Renvoie MAPI_TOP_LEVEL, sauf si indicateurs ont été définis à l’aide de la méthode **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Afficher un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[L’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

