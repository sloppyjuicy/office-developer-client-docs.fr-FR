---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351370"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la taille, en octets, d'un tableau de notifications d'événements et valide la mémoire associée au tableau.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _CNTF_
  
> dans Nombre de structures de [notification](notification.md) dans le tableau indiqué par le paramètre _rgntf_ . 
    
 _rgntf_
  
> dans Pointeur vers le tableau de structures de **notification** dont la taille doit être déterminée. 
    
 _circuits_
  
> remarquer Pointeur facultatif vers la taille, en octets, du tableau désigné par le paramètre _rgntf_ . Si la valeur est NULL, **ScCountNotifications** valide le tableau de notifications. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le nombre a été déterminé avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification incorrecte a été rencontrée.
    
## <a name="remarks"></a>Remarques

Si NULL est transmis dans le paramètre _PCB_ , la fonction **ScCountNotifications** valide uniquement le tableau des notifications, mais aucun décompte n'est réalisé; Si une valeur non null est transmise dans _PCB_, **ScCountNotifications** détermine la taille du tableau et stocke la cause de la _PCB_. Le paramètre _PCB_ doit être assez grand pour contenir l'intégralité du tableau. 
  

