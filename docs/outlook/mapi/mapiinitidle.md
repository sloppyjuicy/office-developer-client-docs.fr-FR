---
title: MAPIInitIdle
description: Décrit la fonction MAPIInitIdle et fournit la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
ms.openlocfilehash: 34184c5d26a3fd6ac266574fb5e3d2675e67acb3
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816121"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise le moteur inactif MAPI pour l’application appelante. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Paramètres

 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **MAPIInitIdle** retourne zéro si l’initialisation réussit, et 1 dans le cas contraire. Si **MAPIInitIdle** est appelé plusieurs fois, tous les appels supplémentaires réussissent, mais sont ignorés, sauf pour incrémenter le nombre de références. 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services doit appeler **MAPIInitIdle** avant d’appeler toute autre fonction de moteur inactive. 
  
Chaque appel à **MAPIInitIdle** doit être mis en correspondance par un appel ultérieur à [MAPIDeInitIdle](mapideinitidle.md), ou le moteur inactif est laissé en cours d’exécution pour l’application appelante. 
  
Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité enregistrée. |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI. |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité inscrite sans la supprimer du système MAPI. |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer. |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur inactif MAPI pour l’application appelante. |
|**MAPIInitIdle** <br/> |Initialise le moteur inactif MAPI pour l’application appelante. |
   
Lorsque toutes les tâches de premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité de priorité la plus élevée qui est prête à s’exécuter. Il n’existe aucune garantie d’ordre d’appel parmi les routines inactives de même priorité. 
  

