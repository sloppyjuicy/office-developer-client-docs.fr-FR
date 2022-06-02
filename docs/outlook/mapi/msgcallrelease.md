---
title: MSGCALLRELEASE
description: MSGCALLRELEASE définit une fonction de rappel qui peut libérer une interface IStorage après la version finale d’un objet IMessage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
ms.openlocfilehash: dde779cd1e912a10723dad103965ffdb2e5a4eb3
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828466"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel qui peut libérer une interface **IStorage** après la publication finale d’un objet **IMessage** créé par-dessus avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Fonction définie implémentée par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par :  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Paramètres

 _ulCallerData_
  
> [in] Contient des informations d’application d’appel sur l’interface **IMessage** . 
    
 _lpMessage_
  
> [in] Pointeur vers le message de niveau supérieur et les pièces jointes qui ont été publiées.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  

