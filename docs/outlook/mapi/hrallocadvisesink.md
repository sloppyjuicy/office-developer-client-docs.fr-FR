---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428899"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de réception de notification, en fonction d’un contexte spécifié par l’implémentation d’appel et d’une fonction de rappel à déclencher par une notification d’événement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameters

 _lpfnCallback_
  
> [in] Pointeur vers une fonction de rappel basée sur le prototype [NOTIFCALLBACK](notifcallback.md) que MAPI doit appeler lorsqu’un événement de notification se produit pour le nouveau réception de notification. 
    
 _lpvContext_
  
> [in] Pointeur vers les données de l’appelant transmises à la fonction de rappel lorsque MAPI l’appelle. Les données de l’appelant peuvent représenter une adresse significative pour le client ou le fournisseur. En règle générale, pour le code C++,  _le paramètre lpvContext_ représente un pointeur vers l’adresse d’un objet. 
    
 _lppAdviseSink_
  
> [out] Pointeur vers un pointeur vers un objet de sink de conseil.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Pour utiliser la fonction **HrAllocAdviseSink,** une application cliente ou un fournisseur de services crée un objet pour recevoir des notifications, crée une fonction de rappel de notification basée sur le prototype de fonction [NOTIFCALLBACK](notifcallback.md) qui va avec cet objet et transmet un pointeur vers l’objet dans la fonction **HrAllocAdviseSink** en tant que valeur _lpvContext._ Cela permet d’effectuer une notification . et dans le cadre du processus de notification, MAPI appelle la fonction de rappel avec le pointeur d’objet comme contexte. 
  
MAPI implémente son moteur de notification de manière asynchrone. En C++, le rappel de notification peut être une méthode objet. Si l’objet générant la notification n’est pas présent, le client ou le fournisseur qui demande la notification doit conserver un nombre de références distinct pour cet objet pour le sink de notification de l’objet. 
  
> [!CAUTION]
> **HrAllocAdviseSink** doit être utilisé avec parcimonie ; il est plus sûr pour les clients de créer leurs propres sinks de conseil. 
  

