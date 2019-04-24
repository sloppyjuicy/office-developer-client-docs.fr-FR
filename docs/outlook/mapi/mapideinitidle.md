---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357322"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Arrête le moteur d'inactivité MAPI pour l'application appelante. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Paramètres

Aucun. 
  
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services doit appeler **MAPIDeInitIdle** lorsqu'il n'a plus besoin du moteur inactif, par exemple lorsqu'il est sur le point d'arrêter le traitement. 
  
Chaque appel à [MAPIInitIdle](mapiinitidle.md) doit être mis en correspondance par un appel ultérieur à **MAPIDeInitIdle**, ou le moteur inactif est laissé en cours d'exécution pour l'application appelante. 
  
Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d'une routine inactive enregistrée.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine inactive inscrite du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l'activer.  <br/> |
|**MAPIDeInitIdle** <br/> |Arrête le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
   
Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter. Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité. 
  

