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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351323"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l'emplacement dans un thread de message auquel un message appartient. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Nombre d'octets dans l'index de conversation parente.
    
 _lpbParent_
  
> dans Pointeur vers des octets dans l'index de conversation parente. Cette valeur peut être NULL si _cbParent_ est égal à zéro. 
    
 _lpcbIndex_
  
> remarquer Pointeur vers le nombre d'octets dans le nouvel index de conversation renvoyé par l'appel. 
    
 _lppbIndex_
  
> remarquer Pointeur vers un pointeur vers le nouvel index de conversation renvoyé par l'appel.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

