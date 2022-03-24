---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Signale l’achèvement du rebasage des rendez-vous.
ms.openlocfilehash: 02fffc62bacbc94a3f652044649628149236d0e0
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63713492"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Signale l’achèvement du rebasage des rendez-vous.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémenté par :  <br/> |Applications clientes MAPI  <br/> |
|Appelé par :  <br/> |Outlook de rebasing  <br/> |
|Type de pointeur :  <br/> |**PFNREBASETASKCOMPLETE** tel que défini dans tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Paramètres

_ulRowIndex_
  
> [in] Ligne qui a été traitée. Cet index fait référence à la structure **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** transmise à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> in] Pointeur vers une structure **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** décrivant l’élément qui a été traitée. 
    
_hrResult_
  
> [in] **HRESULT** indiquant le résultat de l’opération de rebasing. 
    
_fModified_
  
> [in] Spécifie si l’élément a été modifié.
    
_fSentUpdate_
  
> [in] Spécifie si un message de mise à jour de réunion a été envoyé. 
    
_pError_
  
> [in] Pointeur vers une structure **MAPIERROR** avec des informations d’erreur étendues. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Les applications clientes MAPI qui utilisent l’interface [IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour suivre la fin des mises à jour des éléments. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

