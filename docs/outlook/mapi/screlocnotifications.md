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
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415200"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajuste un pointeur dans un tableau de notifications d’événements spécifié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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

 _cntf_
  
> [in] Nombre de structures [DE NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._ 
    
 _rgntf_
  
> [in] Pointeur vers le tableau de **structures DE NOTIFICATION** définissant les notifications d’événement dans lesquelles un pointeur doit être ajusté. 
    
 _pvBaseOld_
  
> [in] Pointeur vers l’adresse de base d’origine du tableau indiquée par le _paramètre rgntf._ 
    
 _pvBaseNew_
  
> [in] Emplacement auquel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiqué par le _paramètre rgntf._ 
    
 _pcb_
  
> [out] Pointeur vers la taille, en octets, du tableau indiqué par le _paramètre pvBaseNew._ 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Un pointeur a été ajusté avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification non valide a été rencontrée.
    
## <a name="remarks"></a>Remarques

Le  _paramètre pcb_ de la **fonction ScRelocNotifications** est facultatif. 
  
## <a name="see-also"></a>Voir aussi



[ScRelocProps](screlocprops.md)

