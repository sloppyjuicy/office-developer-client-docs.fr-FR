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
description: Indique où appartient un message dans un thread de message pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: c4e844b9e6051bc4c68a4cb00de3a261c303d6ae
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405152"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique où appartient un message dans un thread de message. 
  
|Propriété |Valeur |
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
    

