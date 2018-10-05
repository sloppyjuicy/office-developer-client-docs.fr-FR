---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Rapports d’achèvement pour redéfinir des rendez-vous.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388916"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Rapports d’achèvement pour redéfinir des rendez-vous.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémenté par :  <br/> |Applications clientes MAPI  <br/> |
|Appelé par :  <br/> |Objet redéfinition Outlook  <br/> |
|Type de pointeur :  <br/> |**PFNREBASETASKCOMPLETE** comme défini dans tzmovelib.h  <br/> |
   
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
  
> [in] La ligne qui a été traitée. Cet index fait référence à la structure **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** transmise à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> in] pointeur vers une structure **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** qui décrit l’élément qui a été traité. 
    
_hrResult_
  
> [in] Une **valeur HRESULT** indiquant le résultat de l’opération de redéfinition. 
    
_fModified_
  
> [in] Spécifie si l’élément a été modifié.
    
_fSentUpdate_
  
> [in] Spécifie si une réunion mettre à jour le message a été envoyé. 
    
_pError_
  
> [in] Pointeur vers une structure **MAPIERROR** avec des informations d’erreur étendue. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Les applications clientes MAPI qui utilisent l’interface [IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour effectuer le suivi de l’exécution des mises à jour de l’élément. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

