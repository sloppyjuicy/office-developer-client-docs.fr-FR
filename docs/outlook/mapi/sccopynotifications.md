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
ms.openlocfilehash: 28a802ffc43b08d3e2ec2be26dd98fa78f474d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787057"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**S’applique à**: Outlook 
  
Copie un groupe de notifications d’événements dans un bloc de mémoire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ . 
    
 _rgntf_
  
> [in] Pointeur vers un tableau de structures **NOTIFICATION** définissant les notifications d’événements à copier. 
    
 _pvDst_
  
> [out] Pointeur vers les notifications retournées. 
    
 _carte de circuit imprimé_
  
> [out] Facultatif pointeur vers une variable dont la taille, en octets, du tableau indiquée par le paramètre _rgntf_ est stockée. Si ce n’est pas NULL, le paramètre de la _carte de circuits imprimés_ est défini sur le nombre d’octets stocké dans le paramètre _pvDst_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Notifications d’événement ont été copiées avec succès.
    
E_INVALIDARG
  
> Une notification non valide s’est produite.
    
## <a name="remarks"></a>Remarques

Si NULL est indiqué dans le paramètre de la _carte de circuits imprimés_ , aucune copie n’est effectuée ; Si une valeur non nulle est passée dans une _carte de circuit imprimé_, la fonction **ScCopyNotifications** copie la taille du tableau et le tableau lui-même dans un bloc de mémoire. Si la _carte de circuits imprimés_ n’est pas NULL, elle est définie pour le nombre d’octets stocké dans le paramètre _pvDst_ . Le paramètre _pvDst_ doit être suffisant pour contenir l’intégralité du tableau. 
  

