---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: Définit une structure ADRLIST avec le nom spécifié qui contient un nombre spécifié de structures ADRENTRY.
ms.openlocfilehash: 64ef4c9ae16d5a25e073a410ac7aed71a8c47158
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455033"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une structure [ADRLIST](adrlist.md) avec le nom spécifié qui contient un nombre spécifié de structures [ADRENTRY](adrentry.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Paramètres

_ _centries_
  
> Nombre de structures **ADRENTRY** à inclure dans la nouvelle structure **ADRLIST** . 
    
_ _name_
  
> Nom de la nouvelle structure **ADRLIST** . 
    
## <a name="remarks"></a>Remarques

La macro **SizedADRLIST** vous permet de définir une liste de destinataires qui a des limites explicites lorsque des exigences de longueur de tableau sont connues. Le code suivant montre comment caster le résultat de la macro **SizedADRLIST** vers un pointeur de structure **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Voir aussi

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros liées aux structures](macros-related-to-structures.md)

