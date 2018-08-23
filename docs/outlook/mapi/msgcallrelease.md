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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573186"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel que vous pouvez libérer une interface **IStorage** après la version finale d’un objet **IMessage** greffée il avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Fonction implémentée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Paramètres

 _ulCallerData_
  
> [in] Contient des informations d’application appelant sur l’interface **IMessage** . 
    
 _lpMessage_
  
> [in] Pointeur vers le message de niveau supérieur et les pièces jointes qui ont été publiées.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  

