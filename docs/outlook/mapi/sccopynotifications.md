---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435921"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie un groupe de notifications d’événements dans un seul bloc de mémoire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cntf_
  
> [in] Nombre de structures [DE NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._ 
    
 _rgntf_
  
> [in] Pointeur vers un tableau de structures **DE NOTIFICATION** définissant les notifications d’événement à copier. 
    
 _pvDst_
  
> [out] Pointeur vers les notifications renvoyées. 
    
 _pcb_
  
> [out] Pointeur facultatif vers une variable où la taille, en octets, du tableau pointé par le paramètre  _rgntf_ est stockée. Si la valeur n’est pas NULL, le _paramètre pcb_ est définie sur le nombre d’octets stockés dans le _paramètre pvDst._ 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les notifications d’événement ont été correctement copiées.
    
E_INVALIDARG
  
> Une notification non valide a été rencontrée.
    
## <a name="remarks"></a>Remarques

Si null est transmis dans le  _paramètre pcb,_ aucune copie n’est effectuée ; Si une valeur non null est passée dans  _pcb,_ la fonction **ScCopyNotifications** copie la taille du tableau et du tableau lui-même dans un seul bloc de mémoire. Si _pcb n’est_ pas NULL, il est fixé au nombre d’octets stockés dans le _paramètre pvDst._ Le  _paramètre pvDst_ doit être suffisamment grand pour contenir la totalité du tableau. 
  

