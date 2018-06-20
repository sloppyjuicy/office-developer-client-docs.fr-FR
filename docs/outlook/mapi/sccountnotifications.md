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
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787083"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**S’applique à**: Outlook 
  
Détermine la taille, en octets, d’un tableau de notifications d’événements et valide la mémoire associée au tableau.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cntf_
  
> [in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ . 
    
 _rgntf_
  
> [in] Pointeur vers le tableau des structures **NOTIFICATION** dont la taille est déterminée. 
    
 _carte de circuit imprimé_
  
> [out] Pointeur facultatif à la taille, en octets, du tableau indiqué par le paramètre _rgntf_ . Si la valeur NULL, **ScCountNotifications** valide le tableau des notifications. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Count a été correctement déterminé.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification non valide s’est produite.
    
## <a name="remarks"></a>Remarques

Si NULL est indiqué dans le paramètre de la _carte de circuit imprimé_ , la fonction **ScCountNotifications** valide uniquement le tableau des notifications, mais aucun décompte n’effectué ; Si une valeur non nulle est passée dans une _carte de circuit imprimé_, **ScCountNotifications** détermine la taille du tableau et stocke la cause la _carte de circuit imprimé_. Le paramètre de la _carte de circuit imprimé_ doit être suffisant pour contenir l’intégralité du tableau. 
  

