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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339864"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les limites inférieure et supérieure du nombre d'éléments dans l'opération, ainsi que les indicateurs qui contrôlent le mode de calcul des informations d'avancement pour l'opération.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulMin_
  
> dans Pointeur vers une variable qui contient la limite inférieure des éléments de l'opération.
    
 _lpulMax_
  
> dans Pointeur vers une variable qui contient la limite supérieure des éléments de l'opération.
    
 _lpulFlags_
  
> dans Masque de des indicateurs qui contrôle le niveau d'opération sur lequel les informations de progression sont calculées. L'indicateur suivant peut être défini:
    
MAPI_TOP_LEVEL 
  
> Utilise les valeurs des paramètres [méthode imapiprogress::P rogress](imapiprogress-progress.md) de la méthode _ulCount_ et _ulTotal_ , qui indiquent respectivement l'élément traité et le nombre total d'éléments pour incrémenter la progression de l'opération. Lorsque cet indicateur est défini, les valeurs des limites inférieure et supérieure globales doivent être définies. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de services appellent la méthode **méthode imapiprogress:: SetLimits** pour définir ou effacer l'indicateur MAPI_TOP_LEVEL et pour définir les valeurs minimales et maximales locales et globales. La valeur du paramètre flag détermine si l'objet Progress comprend les valeurs minimale et maximale qui doivent être locales ou globales. Lorsque l'indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisées pour calculer la progression de l'opération entière. Les objets Progress initialisent la valeur minimale globale sur 1 et la valeur maximale globale sur 1000. 
  
Lorsque MAPI_TOP_LEVEL n'est pas défini, les valeurs minimale et maximale sont considérées comme locales, et les fournisseurs les utilisent en interne pour afficher la progression des sous-objets de niveau inférieur. Les objets Progress enregistrent uniquement les valeurs minimales et maximales de sorte qu'ils puissent être renvoyés aux fournisseurs lorsque les méthodes [méthode imapiprogress:: GetMin](imapiprogress-getmin.md) et [méthode imapiprogress:: GetMax](imapiprogress-getmax.md) sont appelées. 
  
Pour plus d'informations sur la façon d'implémenter **SetLimits** et les autres méthodes [méthode imapiprogress](imapiprogressiunknown.md) , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: SetLimits  <br/> |MFCMAPI utilise la méthode **méthode imapiprogress:: SetLimits** pour définir les limites et les indicateurs maximaux et minimaux de l'objet Progress.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

