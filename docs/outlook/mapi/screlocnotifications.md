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
description: Ajuste un pointeur dans un tableau de notifications d’événements spécifié pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 2ac94addbfa6a5d3c5b9fd5a4fff4eff8c5c7337
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456286"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajuste un pointeur dans un tableau de notifications d’événements spécifié. 
  
|Propriété |Valeur |
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
  
> [in] Nombre de structures [DE NOTIFICATION](notification.md) dans le tableau indiqué par le  _paramètre rgntf_ . 
    
 _rgntf_
  
> [in] Pointeur vers le tableau de **structures DE NOTIFICATION** définissant les notifications d’événement dans lesquelles un pointeur doit être ajusté. 
    
 _pvBaseOld_
  
> [in] Pointeur vers l’adresse de base d’origine du tableau indiquée par le  _paramètre rgntf_ . 
    
 _pvBaseNew_
  
> [in] Emplacement auquel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiqué par le  _paramètre rgntf_ . 
    
 _pcb_
  
> [out] Pointeur vers la taille, en octets, du tableau indiqué par le  _paramètre pvBaseNew_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Un pointeur a été ajusté avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Une notification non valide a été rencontrée.
    
## <a name="remarks"></a>Remarques

Le  _paramètre pcb_ de la **fonction ScRelocNotifications** est facultatif. 
  
## <a name="see-also"></a>Voir aussi



[ScRelocProps](screlocprops.md)

