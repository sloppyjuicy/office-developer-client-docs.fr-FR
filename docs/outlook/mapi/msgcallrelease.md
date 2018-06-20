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
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784893"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**S’applique à**: Outlook 
  
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
  

