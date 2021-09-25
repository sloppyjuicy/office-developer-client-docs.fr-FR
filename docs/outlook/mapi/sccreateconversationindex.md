---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9c37bd8613f8dc344fad841309b26fb763639935
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609543"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique où appartient un message dans un thread de message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers des octets dans l’index de conversation parent. Cette valeur peut être NULL si  _cbParent_ a la valeur zéro. 
    
 _lpcbIndex_
  
> [out] Pointeur vers le nombre d’octets dans le nouvel index de conversation renvoyé par l’appel. 
    
 _lppbIndex_
  
> [out] Pointeur vers un pointeur vers le nouvel index de conversation renvoyé par l’appel.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

