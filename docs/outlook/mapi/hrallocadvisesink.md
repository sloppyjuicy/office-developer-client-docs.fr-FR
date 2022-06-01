---
title: HrAllocAdviseSink
description: Cet article décrit la fonction HrAllocAdviseSink et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
ms.openlocfilehash: 6077859e39ff29299ad666d947783fd71d73bd5c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816919"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet récepteur de conseils, en fonction d’un contexte spécifié par l’implémentation appelante et d’une fonction de rappel à déclencher par une notification d’événement. 
  
|Propriété |Valeur |
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

## <a name="parameters"></a>Paramètres

 _lpfnCallback_
  
> [in] Pointeur vers une fonction de rappel basée sur le prototype [NOTIFCALLBACK](notifcallback.md) que MAPI doit appeler lorsqu’un événement de notification se produit pour le récepteur de conseils nouvellement créé. 
    
 _lpvContext_
  
> [in] Pointeur vers les données de l’appelant transmises à la fonction de rappel lorsque MAPI les appelle. Les données de l’appelant peuvent représenter une adresse d’importance pour le client ou le fournisseur. En règle générale, pour le code C++, le paramètre  _lpvContext_ représente un pointeur vers l’adresse d’un objet. 
    
 _lppAdviseSink_
  
> [out] Pointeur vers un pointeur vers un objet récepteur conseiller.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Pour utiliser la fonction **HrAllocAdviseSink** , une application cliente ou un fournisseur de services crée un objet pour recevoir des notifications, crée une fonction de rappel de notification basée sur le prototype de fonction [NOTIFCALLBACK](notifcallback.md) qui va avec cet objet et transmet un pointeur à l’objet dans la fonction **HrAllocAdviseSink** comme valeur  _lpvContext_ . Cette opération effectue une notification ; et dans le cadre du processus de notification, MAPI appelle la fonction de rappel avec le pointeur d’objet comme contexte. 
  
MAPI implémente son moteur de notification de manière asynchrone. En C++, le rappel de notification peut être une méthode objet. Si l’objet qui génère la notification n’est pas présent, le client ou le fournisseur qui demande la notification doit conserver un nombre de références distinct pour cet objet pour le récepteur de conseils de l’objet. 
  
> [!CAUTION]
> **HrAllocAdviseSink** doit être utilisé avec parcimonie ; il est plus sûr pour les clients de créer leurs propres récepteurs de conseils. 
  

