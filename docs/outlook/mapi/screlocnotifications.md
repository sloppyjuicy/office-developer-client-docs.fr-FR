---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 03ea2aba27b9ea19daa3ea48f6ae0373f48d49ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591205"
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
  
> [in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._ 
    
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

