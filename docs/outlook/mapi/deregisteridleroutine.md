---
title: DeregisterIdleRoutine
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e77d9a58256b240c45eb106aac1b030b91ee808
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567710"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une routine [d’inactivité basée sur FNIDLE](fnidle.md) du système MAPI. 
  
|||
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

 _ftg_
  
> [in] Balise de fonction qui identifie la routine d’inactivité à supprimer.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Toute tâche d’une application cliente ou d’un fournisseur de services peut désinserrez toute routine inactive pour laquelle elle possède un paramètre  _ftg_ valide. En particulier, une routine inactive peut se désinsister elle-même. 
  
Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine inactive inscrite.  <br/> |
|**DeregisterIdleRoutine** <br/> |Supprime une routine d’inactivité enregistrée du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application à l’appel.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application à l’appel.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** et **EnableIdleRoutine** prennent comme paramètre d’entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté. Il n’existe aucune garantie d’appel de l’ordre parmi les routines inactives de la même priorité. 
  
Une fois la routine inactive désinserrée, le moteur inactif ne l’appelle plus. Toute implémentation qui appelle **DeregisterIdleRoutine** doit désaffecter les blocs de mémoire vers lesquels elle a transmis des pointeurs pour que le moteur inactif utilise dans son appel d’origine à la fonction **FtgRegisterIdleRoutine.** 
  

