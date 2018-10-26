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
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567236"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le nombre maximal d’éléments dans l’opération de l’avancement des informations s’affichent.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Paramètres

 _lpulMax_
  
> [out] Pointeur vers le nombre maximal d’éléments dans l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre maximal d’éléments dans l’opération a été récupéré.
    
## <a name="remarks"></a>Remarques

La valeur maximale représente la fin de l’opération sous forme numérique. La valeur peut être une valeur maximale globale, utilisée pour représenter l’étendue de l’intégralité de l’affichage de la progression, ou une valeur locale, utilisée pour représenter uniquement une partie de l’affichage. 
  
La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend la valeur maximale à être local ou global. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur maximale est considéré comme étant global et est utilisée pour calculer l’avancement pour toute l’opération. Lorsque MAPI_TOP_LEVEL n’est pas définie, la valeur maximale est considéré comme étant local, et fournisseurs de l’utiliser en interne pour afficher la progression de sous-objets de niveau inférieurs. Objets de progression enregistrement la valeur maximale locale uniquement pour renvoyer à un fournisseur via un appel **GetMax** . 
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Initialiser la valeur maximale et 1000. Les fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **GetMax** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::GetMax** pour obtenir la valeur maximale pour l’objet de progression. Renvoie 1000, sauf si les limites précédemment ont été définies avec la méthode **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

