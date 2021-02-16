---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Signale l’avancement de l’éumération et de la rebasation des rendez-vous.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326452"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Signale l’avancement de l’éumération et de la rebasation des rendez-vous.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémenté par :  <br/> |Applications clientes MAPI  <br/> |
|Appelé par :  <br/> |Objet rebasing Outlook  <br/> |
|Type de pointeur :  <br/> |**PFNREBASETASKPROGRESS** tel que défini dans tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Paramètres

_ulMin_
  
> [in] Bas de la plage de rendez-vous en cours de traitement. Il est généralement zéro.
    
_ulMax_
  
> [in] Fin de la plage de rendez-vous en cours de traitement. Il s’agit généralement du nombre d’éléments du dossier calendrier en cours de traitement.
    
_ulCur_
  
> [in] Élément actuel en cours de traitement.
    
_État_
  
> [in] Valeur qui indique l’état de l’élément en cours de traitement. L’REBASE_APPT_STATE **est** définie dans tzmovelib.h.  _State_ est l'une des valeurs suivantes : 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** : analyse et examen d’un élément. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** : analyse et recherche d’un élément. 
    
   - **REBASE_APPT_STATE_BEGIN** : correction et démarrage d’un élément. 
    
   - **REBASE_APPT_STATE_REBASING** : correction et ajustement d’un élément. 
    
   - **REBASE_APPT_STATE_SENDING** : correction et envoi d’une mise à jour de réunion. 
    
   - **REBASE_APPT_STATE_DONE** : correction et fin d’un élément. 
    
_pRowCur_
  
> [in] Pointeur vers une structure **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** qui décrit l’élément en cours d’analyse ou de correction. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Les applications clientes MAPI qui utilisent [l’interface IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour suivre le traitement des éléments. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

