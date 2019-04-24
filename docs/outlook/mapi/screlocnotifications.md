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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360710"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajuste un pointeur dans un tableau de notification d'événement spécifié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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

 _CNTF_
  
> dans Nombre de structures de [notification](notification.md) dans le tableau indiqué par le paramètre _rgntf_ . 
    
 _rgntf_
  
> dans Pointeur vers le tableau de structures de **notification** définissant des notifications d'événement dans lesquelles un pointeur doit être ajusté. 
    
 _pvBaseOld_
  
> dans Pointeur vers l'adresse de base d'origine du tableau indiquée par le paramètre _rgntf_ . 
    
 _pvBaseNew_
  
> dans Emplacement auquel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiquée par le paramètre _rgntf_ . 
    
 _circuits_
  
> remarquer Pointeur vers la taille, en octets, du tableau indiqué par le paramètre _pvBaseNew_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Un pointeur a été ajusté avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification incorrecte a été rencontrée.
    
## <a name="remarks"></a>Remarques

Le paramètre _PCB_ de la fonction **ScRelocNotifications** est facultatif. 
  
## <a name="see-also"></a>Voir aussi



[ScRelocProps](screlocprops.md)

