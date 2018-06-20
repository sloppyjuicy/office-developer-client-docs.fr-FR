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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787077"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**S’applique à**: Outlook 
  
Indique où dans un thread de message, un message appartient. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

