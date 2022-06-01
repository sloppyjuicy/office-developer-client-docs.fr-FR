---
title: MAPIDeInitIdle
description: Décrit la fonction MAPIDeInitIdle et fournit la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
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
ms.openlocfilehash: 58fc969f75cff31becb11c1fb7b5142372a3ee9a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818130"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Arrête le moteur inactif MAPI pour l’application appelante. 
  
|Propriété |Valeur |
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
  
Chaque appel à [MAPIInitIdle](mapiinitidle.md) doit être mis en correspondance par un appel ultérieur à **MAPIDeInitIdle**, ou le moteur inactif est laissé en cours d’exécution pour l’application appelante. 
  
Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité enregistrée. |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI. |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité inscrite sans la supprimer du système MAPI. |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer. |
|**MAPIDeInitIdle** <br/> |Arrête le moteur inactif MAPI pour l’application appelante. |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur inactif MAPI pour l’application appelante. |
   
Lorsque toutes les tâches de premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité de priorité la plus élevée qui est prête à s’exécuter. Il n’existe aucune garantie d’ordre d’appel parmi les routines inactives de même priorité. 
  

