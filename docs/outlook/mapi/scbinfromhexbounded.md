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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357497"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ConVertit la partie spécifiée d'une représentation sous forme de chaîne d'un nombre hexadécimal en nombre binaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Paramètres

 _t_
  
> dans Pointeur vers la chaîne terminée par un caractère null à convertir. Les caractères valides incluent les caractères hexadécimaux compris entre 0 et 9, ainsi que les caractères majuscules et minuscules a à f.
    
 _pb_
  
> remarquer Pointeur vers le nombre binaire renvoyé.
    
 _cb_
  
> dans Taille, en octets, du paramètre _PB_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La conversion a réussi.
    
MAPI_E_CALL_FAILED
  
> Des caractères non valides ont été détectés.
    
## <a name="see-also"></a>Voir aussi



[FBinFromHex](fbinfromhex.md)

