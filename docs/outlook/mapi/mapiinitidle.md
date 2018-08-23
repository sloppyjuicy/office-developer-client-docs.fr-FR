---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fd9a91b089bb06e6dfe34a1a144245d404adb270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569224"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Initialise le moteur d’inactivité MAPI pour l’application appelante. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Paramètres

 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **MAPIInitIdle** renvoie zéro si l’initialisation réussit et 1 dans le cas contraire. Si **MAPIInitIdle** est appelée plusieurs fois, tous les appels supplémentaires réussissent, mais sont ignorés sauf to incrémente le décompte de références. 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services doit appeler **MAPIInitIdle** avant d’appeler toute autre fonction moteur inactif. 
  
Chaque appel à **MAPIInitIdle** doit correspondre à un autre appel à [MAPIDeInitIdle](mapideinitidle.md), ou le moteur d’inactivité est de gauche en cours d’exécution pour l’application appelante. 
  
Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrit.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité inscrit dans le système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
|**MAPIInitIdle** <br/> |Initialise le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
   
Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter. Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité. 
  

