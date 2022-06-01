---
title: DeregisterIdleRoutine
description: DeregisterIdleRoutine supprime une routine d’inactivité basée sur FNIDLE du système MAPI. Cet article décrit ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
ms.openlocfilehash: a8746a91b8b23c550fd575b0b5867d060150a326
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817122"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une routine d’inactivité basée sur [FNIDLE](fnidle.md) du système MAPI. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Paramètres

 _Ftg_
  
> [in] Balise de fonction qui identifie la routine inactive à supprimer.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Toute tâche d’une application cliente ou d’un fournisseur de services peut annuler l’inscription de toute routine inactive pour laquelle elle a un paramètre  _ftg_ valide. En particulier, une routine inactive peut se désinscrire elle-même. 
  
Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité enregistrée. |
|**DeregisterIdleRoutine** <br/> |Supprime une routine d’inactivité enregistrée du système MAPI. |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité inscrite sans la supprimer du système MAPI. |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer. |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur inactif MAPI pour l’application appelante. |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur inactif MAPI pour l’application appelante. |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** et **EnableIdleRoutine** prennent comme paramètre d’entrée la balise de fonction retournée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité de priorité la plus élevée qui est prête à s’exécuter. Il n’existe aucune garantie d’ordre d’appel parmi les routines inactives de même priorité. 
  
Une fois la routine inactive désinscrite, le moteur inactif ne l’appelle plus. Toute implémentation qui appelle **DeregisterIdleRoutine** doit libérer tous les blocs de mémoire auxquels il a passé des pointeurs pour que le moteur inactif soit utilisé dans son appel d’origine à la fonction **FtgRegisterIdleRoutine** . 
  

