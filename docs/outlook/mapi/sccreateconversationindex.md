---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594150"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique où dans un thread de message, un message appartient. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>Paramètres

 _cbParent_
  
> [in] Nombre d’octets dans l’index de conversation parent.
    
 _lpbParent_
  
> [in] Pointeur vers les octets dans l’index de conversation parent. Cela peut être NULL si _cbParent_ est égale à zéro. 
    
 _lpcbIndex_
  
> [out] Pointeur vers le nombre d’octets dans le nouvel index de conversation renvoyé par l’appel. 
    
 _lppbIndex_
  
> [out] Pointeur vers un pointeur vers le nouvel index de conversation renvoyé par l’appel.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

