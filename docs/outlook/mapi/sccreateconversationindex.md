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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415655"
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

## <a name="parameters"></a>Parameters

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
    

