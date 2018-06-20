---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Indique la progression de l’énumération et redéfinition de rendez-vous.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782831"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Indique la progression de l’énumération et redéfinition de rendez-vous.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémentée par :  <br/> |Applications clientes MAPI  <br/> |
|Appelée par :  <br/> |Objet redéfinition Outlook  <br/> |
|Type de pointeur :  <br/> |**PFNREBASETASKPROGRESS** comme défini dans tzmovelib.h  <br/> |
   
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
  
> [in] Le début de la plage de rendez-vous en cours de traitement. Il est généralement égale à zéro.
    
_ulMax_
  
> [in] Haut de gamme de la plage de rendez-vous en cours de traitement. Il est généralement le nombre d’éléments dans le dossier de calendrier en cours de traitement.
    
_ulCur_
  
> [in] L’élément actuel en cours de traitement.
    
_State_
  
> [in] Une valeur qui indique l’état de l’élément en cours de traitement. L’énumération **REBASE_APPT_STATE** est définie dans tzmovelib.h.  _État_ est une des valeurs suivantes : 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** — analyse et en examinant un élément. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** — analyse et a trouvé un élément. 
    
   - **REBASE_APPT_STATE_BEGIN** — fixation et démarrage d’un élément. 
    
   - **REBASE_APPT_STATE_REBASING** — fixation et ajustement d’un élément. 
    
   - **REBASE_APPT_STATE_SENDING** — fixation et l’envoi d’une mise à jour de réunion. 
    
   - **REBASE_APPT_STATE_DONE** — fixation et terminé avec un élément. 
    
_pRowCur_
  
> [in] Pointeur vers une structure **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** qui décrit l’élément en cours d’analyse ou fixe. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Les applications clientes MAPI qui utilisent l’interface [IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour effectuer le suivi du traitement de l’élément. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

