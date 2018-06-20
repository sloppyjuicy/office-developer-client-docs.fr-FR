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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783879"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**S’applique à**: Outlook 
  
Renvoie le nombre maximal d’éléments dans l’opération de l’avancement des informations s’affichent.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Paramètres

 _lpulMax_
  
> [out] Pointeur vers le nombre maximal d’éléments dans l’opération.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le nombre maximal d’éléments dans l’opération a été récupéré.
    
## <a name="remarks"></a>Remarques

La valeur maximale représente la fin de l’opération sous forme numérique. La valeur peut être une valeur maximale globale, utilisé pour représenter l’étendue de l’affichage de la progression de l’intégralité ou une valeur locale, utilisé pour ne représenter qu’une partie de l’affichage. 
  
La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend la valeur maximale à être local ou global. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur maximale est considéré comme étant global et est utilisée pour calculer l’avancement pour toute l’opération. Lorsque MAPI_TOP_LEVEL n’est pas définie, la valeur maximale est considéré comme étant local, et fournisseurs de l’utiliser en interne pour afficher la progression de sous-objets de niveau inférieurs. Objets de progression enregistrement la valeur maximale locale uniquement pour renvoyer à un fournisseur via un appel **GetMax** . 
  
Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Initialiser la valeur maximale et 1000. Fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **GetMax** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::GetMax** pour obtenir la valeur maximale pour l’objet de progression. Renvoie 1000, sauf si les limites précédemment ont été définies avec la méthode **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Afficher un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[L’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

