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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357483"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie un groupe de notifications d'événements dans un seul bloc de mémoire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

 _CNTF_
  
> dans Nombre de structures de [notification](notification.md) dans le tableau indiqué par le paramètre _rgntf_ . 
    
 _rgntf_
  
> dans Pointeur vers un tableau de structures de **notification** définissant les notifications d'événement à copier. 
    
 _pvDst_
  
> remarquer Pointeur vers les notifications renvoyées. 
    
 _circuits_
  
> remarquer Pointeur facultatif vers une variable où la taille, en octets, du tableau désigné par le paramètre _rgntf_ est stockée. Si la valeur n'est pas NULL, le paramètre _PCB_ est défini sur le nombre d'octets stockés dans le paramètre _pvDst_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les notifications d'événement ont été correctement copiées.
    
E_INVALIDARG
  
> Une notification incorrecte a été rencontrée.
    
## <a name="remarks"></a>Remarques

Si NULL est transmis dans le paramètre _PCB_ , aucune copie n'est effectuée; Si une valeur non null est transmise dans _PCB_, la fonction **ScCopyNotifications** copie la taille du tableau et le tableau lui-même dans un bloc de mémoire unique. Si _PCB_ n'est pas null, il est défini sur le nombre d'octets stockés dans le paramètre _pvDst_ . Le paramètre _pvDst_ doit être suffisamment grand pour contenir l'intégralité du tableau. 
  

