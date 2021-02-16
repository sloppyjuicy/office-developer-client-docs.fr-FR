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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437993"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la taille, en octets, d’un tableau de notifications d’événements et valide la mémoire associée au tableau.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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

 _cntf_
  
> [in] Nombre de structures [DE NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._ 
    
 _rgntf_
  
> [in] Pointeur vers le tableau des structures **DE NOTIFICATION** dont la taille doit être déterminée. 
    
 _pcb_
  
> [out] Pointeur facultatif vers la taille, en octets, du tableau pointé par le _paramètre rgntf._ Si la valeur est NULL, **ScCountNotifications** valide le tableau des notifications. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le nombre a été déterminé avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification non valide a été rencontrée.
    
## <a name="remarks"></a>Remarques

Si NULL est transmis dans le  _paramètre pcb,_ la **fonction ScCountNotifications** valide uniquement le tableau de notifications, mais aucun décompte n’est effectué . si une valeur non null est passée dans  _pcb_, **ScCountNotifications** détermine la taille du tableau et stocke la  _cause pcb_. Le  _paramètre pcb_ doit être suffisamment grand pour contenir la totalité du tableau. 
  

