---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589279"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Convertit la partie spécifiée d’une représentation de chaîne d’un nombre hexadécimal en nombre binaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Paramètres

 _sz_
  
> [in] Pointeur vers la chaîne à convertir. Caractères valides incluent les caractères hexadécimaux 0 à 9 et les deux caractères majuscules et minuscules d’a à f.
    
 _pb_
  
> [out] Pointeur vers le nombre binaire renvoyé.
    
 _cb_
  
> [in] Taille, en octets, du paramètre _po_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Conversion a réussi.
    
MAPI_E_CALL_FAILED
  
> Caractères non valides se sont produites.
    
## <a name="see-also"></a>Voir aussi



[FBinFromHex](fbinfromhex.md)

