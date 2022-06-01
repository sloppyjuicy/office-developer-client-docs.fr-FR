---
title: EnableIdleRoutine
description: EnableIdleRoutine active ou désactive une routine d’inactivité basée sur FNIDLE. Cet article décrit sa syntaxe, ses paramètres et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
ms.openlocfilehash: ac0960b8c21ec313d9dfc6bf5fe1469b43b6b0d5
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816681"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active ou désactive une routine d’inactivité basée sur [FNIDLE](fnidle.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Paramètres

 _Ftg_
  
> [in] Balise de fonction qui identifie la routine inactive à activer ou à désactiver. 
    
 _fEnable_
  
> [in] Contient TRUE si le moteur inactif doit activer la routine d’inactivité, ou FALSE s’il doit la désactiver.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité enregistrée. |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI. |
|**EnableIdleRoutine** <br/> |Désactive ou réactive une routine d’inactivité inscrite sans la supprimer du système MAPI. |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer. |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur inactif MAPI pour l’application appelante. |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur inactif MAPI pour l’application appelante. |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** et **EnableIdleRoutine** prennent comme paramètre d’entrée la balise de fonction retournée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité de priorité la plus élevée qui est prête à s’exécuter. Il n’existe aucune garantie d’ordre d’appel parmi les routines inactives de même priorité. 
  

