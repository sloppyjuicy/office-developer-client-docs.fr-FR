---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583966"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajuste un pointeur au sein d’un tableau de notification d’événement spécifié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cntf_
  
> [in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ . 
    
 _rgntf_
  
> [in] Pointeur vers le tableau des structures **NOTIFICATION** définition des notifications d’événement dans lequel un pointeur doit être ajustées. 
    
 _pvBaseOld_
  
> [in] Pointeur vers l’adresse de base d’origine du tableau indiquée par le paramètre _rgntf_ . 
    
 _pvBaseNew_
  
> [in] L’emplacement dans lequel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiquée par le paramètre _rgntf_ . 
    
 _carte de circuit imprimé_
  
> [out] Pointeur vers la taille, en octets, du tableau indiquée par le paramètre _pvBaseNew_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Un pointeur ajusté avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification non valide s’est produite.
    
## <a name="remarks"></a>Remarques

Le paramètre de la _carte de circuits imprimés_ à la fonction **ScRelocNotifications** est facultatif. 
  
## <a name="see-also"></a>Voir aussi



[ScRelocProps](screlocprops.md)

