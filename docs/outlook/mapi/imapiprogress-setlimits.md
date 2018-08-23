---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 010f69b70324d4280a34d2fe06d670e07d922d86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586773"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit les limites supérieures et inférieures pour le nombre d’éléments dans l’opération et des indicateurs qui déterminent comment les informations d’avancement sont calculées pour l’opération.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulMin_
  
> [in] Pointeur vers une variable qui contient la limite inférieure d’éléments dans l’opération.
    
 _lpulMax_
  
> [in] Pointeur vers une variable qui contient la limite supérieure d’éléments dans l’opération.
    
 _lpulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le niveau de l’opération sur l’avancement des informations sont calculées. Vous pouvez définir l’indicateur suivant :
    
MAPI_TOP_LEVEL 
  
> Utilise les valeurs de paramètres de la méthode [IMAPIProgress::Progress](imapiprogress-progress.md) de _ulCount_ et _ulTotal_ , qui indiquent l’élément en cours de traitement et le nombre total d’éléments, respectivement, au cours d’incrémentation sur l’opération. Lorsque cet indicateur est défini, les valeurs des limites inférieures et supérieures globales doivent être définies. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs de services appeler la méthode **IMAPIProgress::SetLimits** pour définir ou effacer l’indicateur MAPI_TOP_LEVEL et définir les valeurs minimales et maximales globales et locales. La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend les valeurs minimales et maximales pour être local ou global. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisés pour calculer l’avancement pour toute l’opération. Objets de progression initialiser la valeur minimale globale à 1 et la valeur maximale globale et 1000. 
  
Lorsque MAPI_TOP_LEVEL n’est pas définie, les valeurs minimales et maximales sont considérées comme locales et fournisseurs de les utilisent en interne pour afficher la progression de sous-objets de niveau inférieurs. Objets de progression enregistrement les valeurs minimales et maximales locales uniquement afin qu’ils peuvent être renvoyées à fournisseurs lorsque les méthodes [IMAPIProgress::GetMin](imapiprogress-getmin.md) et [IMAPIProgress::GetMax](imapiprogress-getmax.md) sont appelées. 
  
Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **SetLimits** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::SetLimits** pour définir les indicateurs pour l’objet de l’avancement des limites maximale et minimale.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Afficher un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

