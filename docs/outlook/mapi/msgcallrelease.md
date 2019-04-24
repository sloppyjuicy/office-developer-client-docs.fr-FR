---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338562"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel qui peut libérer une interface **IStorage** après la publication de la version finale d'un objet **IMessage** basée dessus avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage. h  <br/> |
|Fonction définie implémentée par:  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Paramètres

 _ulCallerData_
  
> dans Contient des informations sur l'application appelante à propos de l'interface **IMessage** . 
    
 _lpMessage_
  
> dans Pointeur vers le message de niveau supérieur et pièces jointes qui ont été publiées.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  

