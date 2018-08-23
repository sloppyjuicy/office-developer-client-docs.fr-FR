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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589321"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée un objet récepteur advise, étant donné un contexte spécifié par l’implémentation d’appel et une fonction de rappel pour être déclenché par une notification d’événement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Paramètres

 _lpfnCallback_
  
> [in] Pointeur vers une fonction de rappel selon le prototype [NOTIFCALLBACK](notifcallback.md) MAPI consiste à appeler lorsque cet événement se produit un événement de notification pour le récepteur de notification nouvellement créé. 
    
 _lpvContext_
  
> [in] Pointeur vers les données de l’appelant transmis à la fonction de rappel lorsque MAPI il l’appelle. Les données de l’appelant peuvent représenter une adresse de l’argument précision pour le client ou le fournisseur. En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers l’adresse d’un objet. 
    
 _lppAdviseSink_
  
> [out] Pointeur vers un pointeur vers un objet de réception de notifications.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Pour utiliser la fonction **HrAllocAdviseSink** , une application cliente ou un fournisseur de services crée un objet pour recevoir des notifications, crée une fonction de rappel de notification basée sur le prototype de fonction [NOTIFCALLBACK](notifcallback.md) qui accompagne cet objet, et passe un pointeur vers l’objet dans la fonction **HrAllocAdviseSink** en tant que la valeur _lpvContext_ . Cela effectue une notification ; et, dans le cadre du processus de notification, les appels MAPI avec le pointeur de l’objet en tant que le contexte de la fonction de rappel. 
  
MAPI implémente le moteur de notification asynchrone. En C++, le rappel de notification peut être une méthode d’objet. Si l’objet de génération de la notification n’est pas présent, le client ou le fournisseur demande de notification doit conserver un décompte de références distincte pour cet objet de l’objet récepteur de notification. 
  
> [!CAUTION]
> **HrAllocAdviseSink** doit être utilisé avec modération ; Il est recommandé pour les clients créer leurs propres récepteurs advise. 
  

