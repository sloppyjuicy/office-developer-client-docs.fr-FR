---
title: MAPIInitIdle
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 43b5168f1d29ead887f884e6c61456c5ab28364b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575483"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise le moteur d’inactivité MAPI pour l’application à l’appel. 
  
|||
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

La **fonction MAPIInitIdle** renvoie zéro si l’initialisation réussit et 1 dans le cas contraire. Si **MAPIInitIdle** est appelé plusieurs fois, tous les appels supplémentaires aboutit mais sont ignorés, sauf pour incrémenter le nombre de références. 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services doit appeler **MAPIInitIdle** avant d’appeler toute autre fonction de moteur inactive. 
  
Chaque appel **à MAPIInitIdle** doit être suivi d’un appel ultérieur à [MAPIDeInitIdle](mapideinitidle.md)ou le moteur inactif reste en cours d’exécution pour l’application d’appel. 
  
Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine inactive inscrite.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application à l’appel.  <br/> |
|**MAPIInitIdle** <br/> |Initialise le moteur d’inactivité MAPI pour l’application à l’appel.  <br/> |
   
Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté. Il n’existe aucune garantie d’appel de l’ordre parmi les routines inactives de la même priorité. 
  

