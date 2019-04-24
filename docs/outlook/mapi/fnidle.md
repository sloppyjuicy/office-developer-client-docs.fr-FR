---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342244"
---
# <a name="fnidle"></a>FNIDLE
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une routine inactive appelée périodiquement par le moteur inactif MAPI en fonction de la priorité. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Fonction définie implémentée par:  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par:  <br/> |MAPI  <br/> |
|Type de pointeur correspondant:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Paramètres

 _lpvContext_
  
> dans Pointeur vers un bloc de mémoire que MAPI transmet à la routine inactive chaque fois qu'il l'appelle. Ce pointeur est transmis au moteur inactif MAPI dans le paramètre _pvIdleParam_ par [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Les données du bloc de mémoire peuvent fournir un contexte pour l'appel à la routine inactive, par exemple l'objet sur lequel agir, ou l'état actuel d'une longue opération.
    
## <a name="return-value"></a>Valeur renvoyée

FALSE 
  
> Une routine inactive avec le prototype **FNIDLE** doit toujours renvoyer la valeur false. 
    
## <a name="remarks"></a>Remarques

La fonctionnalité spécifique de la routine inactive est déterminée par l'application cliente ou le fournisseur de services. 
  
Le client ou le fournisseur doit limiter le temps d'exécution de chaque État d'une routine inactive. Chaque État doit effectuer une quantité minimale de traitement, mettre à jour l'état actuel dans les données de contexte pointées par _lpvContext_, puis revenir au moteur d'inactivité MAPI. 
  
Le client ou le fournisseur doit appeler la fonction MAPI [MAPIInitIdle](mapiinitidle.md) pour pouvoir inscrire sa propre routine inactive avec un appel à la fonction [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction FNIDLE: 
  
|**Fonction de routine inactive**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d'une routine inactive enregistrée.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine inactive inscrite du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l'activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter. Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité. 
  

