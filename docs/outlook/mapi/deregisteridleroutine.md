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
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783155"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**S’applique à**: Outlook 
  
Supprime un [FNIDLE](fnidle.md) en fonction de routine inactive à partir du système MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Paramètres

 _ftg_
  
> [in] Balise de fonction qui identifie la routine inactive à supprimer.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une tâche dans une application cliente ou d’un fournisseur de services peut annuler l’enregistrement d’une routine inactive pour lequel elle possède un paramètre valide _ftg_ . En particulier, une routine inactive peut désinscrire lui-même. 
  
Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrit.  <br/> |
|**DeregisterIdleRoutine** <br/> |Supprime une routine d’inactivité inscrit dans le système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter. Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité. 
  
Une fois la routine inactive inscription est désactivée, le moteur d’inactivité n’appelle pas il à nouveau. Une implémentation qui appelle **DeregisterIdleRoutine** doit libérer tous les blocs de mémoire à laquelle il passé pointeurs moteur inactif à utiliser dans son appel à la fonction **FtgRegisterIdleRoutine** d’origine. 
  

