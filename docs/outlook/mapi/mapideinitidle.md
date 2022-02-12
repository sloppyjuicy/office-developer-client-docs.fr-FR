---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b19b9d2d453837ba7b9668ccfa042f04ef4c9e10
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776227"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Arrête le moteur d’inactivité MAPI pour l’application à l’appel. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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

Une application cliente ou un fournisseur de services doit appeler **MAPIDeInitIdle** lorsqu’il n’a plus besoin du moteur inactif, par exemple, lorsqu’il est sur le point d’arrêter le traitement. 
  
Chaque appel [à MAPIInitIdle](mapiinitidle.md) doit être suivi d’un appel ultérieur à **MAPIDeInitIdle**, sinon le moteur inactif reste en cours d’exécution pour l’application d’appel. 
  
Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrite. |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI. |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI. |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer. |
|**MAPIDeInitIdle** <br/> |Arrête le moteur d’inactivité MAPI pour l’application à l’appel. |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application à l’appel. |
   
Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté. Il n’existe aucune garantie d’appel d’ordre parmi les routines inactives de la même priorité. 
  

