---
title: MSGCALLRELEASE
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 41176f8f53ed9ea167580d401539e249399f08a2
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720165"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel qui peut libérer une interface **IStorage** après la version finale d’un objet **IMessage** créé au-dessus avec la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
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
  
> [in] Contient des informations d’application d’appel sur **l’interface IMessage** . 
    
 _lpMessage_
  
> [in] Pointeur vers le message de niveau supérieur et les pièces jointes qui ont été libérées.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  

