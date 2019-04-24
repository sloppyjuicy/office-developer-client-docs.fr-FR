---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316799"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une routine inactive basée sur [FNIDLE](fnidle.md) du système MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Paramètres

 _FTG_
  
> dans Balise de fonction qui identifie la routine inactive à supprimer.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Toute tâche dans une application cliente ou un fournisseur de services peut annuler l'inscription de toute routine inactive pour laquelle il a un paramètre _FTG_ valide. En particulier, une routine inactive peut se déregistrer elle-même. 
  
Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d'une routine inactive enregistrée.  <br/> |
|**DeregisterIdleRoutine** <br/> |Supprime une routine inactive inscrite du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l'activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter. Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité. 
  
Une fois la routine inactive désinscrite, le moteur inactif ne le rappelle pas. Toute implémentation qui appelle **DeregisterIdleRoutine** doit annuler l'allocation des blocs de mémoire auxquels elle a passé des pointeurs pour le moteur inactif afin de l'utiliser dans son appel d'origine à la fonction **FtgRegisterIdleRoutine** . 
  

