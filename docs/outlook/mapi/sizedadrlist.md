---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574740"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une structure [ADRLIST](adrlist.md) avec le nom spécifié qui contient un nombre spécifié de structures [ADRENTRY](adrentry.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Paramètres

__centries_
  
> Nombre de structures **ADRENTRY** à inclure dans la nouvelle structure **ADRLIST** . 
    
__nom_
  
> Nom de la nouvelle structure **ADRLIST** . 
    
## <a name="remarks"></a>Remarques

La macro **SizedADRLIST** vous permet de définir une liste de destinataires qui a des limites explicites lorsque les besoins en matière de longueur de tableau. Le code suivant montre comment convertir le résultat de la macro **SizedADRLIST** vers un pointeur de structure **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Voir aussi

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros liées aux structures](macros-related-to-structures.md)

