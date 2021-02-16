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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423460"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une structure [ADRLIST](adrlist.md) avec le nom spécifié qui contient un nombre spécifié de structures [ADRENTRY.](adrentry.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Paramètres

_ _centries_
  
> Nombre de structures **ADRENTRY** à inclure dans la nouvelle structure **ADRLIST.** 
    
_ _name_
  
> Nom de la nouvelle structure **ADRLIST.** 
    
## <a name="remarks"></a>Remarques

La macro **SizedADRLIST** vous permet de définir une liste de destinataires qui a des limites explicites lorsque des exigences de longueur de tableau sont connues. Le code suivant montre comment caster le résultat de la macro **SizedADRLIST** vers un pointeur de structure **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Voir aussi

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros liées aux structures](macros-related-to-structures.md)

