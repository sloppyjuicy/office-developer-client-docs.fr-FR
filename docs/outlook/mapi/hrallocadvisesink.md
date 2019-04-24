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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348215"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de récepteur de notifications, en fonction d'un contexte spécifié par l'implémentation de l'appel et d'une fonction de rappel à déclencher par une notification d'événement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Paramètres

 _lpfnCallback_
  
> dans Pointeur vers une fonction de rappel basée sur le prototype [NOTIFCALLBACK](notifcallback.md) que MAPI doit appeler lorsqu'un événement de notification se produit pour le récepteur de notifications nouvellement créé. 
    
 _lpvContext_
  
> dans Pointeur vers les données d'appelant transmises à la fonction de rappel lorsque MAPI les appelle. Les données de l'appelant peuvent représenter une adresse de signification pour le client ou le fournisseur. En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers l'adresse d'un objet. 
    
 _lppAdviseSink_
  
> remarquer Pointeur vers un pointeur vers un objet de récepteur de notifications.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Pour utiliser la fonction **HrAllocAdviseSink** , une application cliente ou un fournisseur de services crée un objet pour recevoir des notifications, crée une fonction de rappel de notification basée sur le prototype de fonction [NOTIFCALLBACK](notifcallback.md) qui suit cet objet, et transmet un pointeur vers l'objet dans la fonction **HrAllocAdviseSink** en tant que valeur _lpvContext_ . Cette opération effectue une notification; dans le cadre du processus de notification, MAPI appelle la fonction de rappel avec le pointeur d'objet comme contexte. 
  
MAPI implémente le moteur de notification de manière asynchrone. En C++, le rappel de notification peut être une méthode d'objet. Si l'objet qui génère la notification n'est pas présent, le client ou le fournisseur qui demande la notification doit conserver un nombre de référence distinct pour cet objet pour le récepteur de notification de l'objet. 
  
> [!CAUTION]
> **HrAllocAdviseSink** doit être utilisé avec modération; Il est plus sûr pour les clients de créer leurs propres récepteurs de notification. 
  

