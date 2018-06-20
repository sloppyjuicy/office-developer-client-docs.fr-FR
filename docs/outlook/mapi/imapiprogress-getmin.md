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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783882"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**S’applique à**: Outlook 
  
Renvoie la valeur minimale dans la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) pour l’avancement des informations s’affichent. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Paramètres

 _lpulMin_
  
> [out] Pointeur vers le nombre minimal d’éléments dans l’opération.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le nombre minimal d’éléments dans l’opération a été récupéré.
    
## <a name="remarks"></a>Remarques

La valeur minimale représente le début de l’opération sous forme numérique. La valeur peut être une valeur maximale globale, utilisé pour représenter l’étendue de l’affichage de la progression de l’intégralité ou une valeur locale, utilisé pour ne représenter qu’une partie de l’affichage. 
  
La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend la valeur minimale pour être local ou global. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur minimale est considéré comme étant global et est utilisée pour calculer l’avancement pour toute l’opération. Lorsque MAPI_TOP_LEVEL n’est pas définie, la valeur minimale est considérée comme étant locale et fournisseurs de l’utiliser en interne pour afficher la progression de sous-objets de niveau inférieurs. Objets de progression enregistrement la valeur minimale locale uniquement pour renvoyer à un fournisseur via un appel **GetMin** . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Initialiser la valeur minimale 1. Fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode **IMAPIProgress::SetLimits** . Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **GetMin** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::GetMin** pour obtenir la valeur minimale pour l’indicateur de progression. Renvoie la valeur 1, sauf si la limite a été définie précédemment en appelant la méthode **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Afficher un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[L’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

