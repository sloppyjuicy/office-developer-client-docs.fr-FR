---
title: CheckParameters
description: CheckParameters appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
ms.openlocfilehash: c1e63e37b993dcef4602e0ed67e4acf4752ac273
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816247"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par énumération, la méthode à valider. 
    
 _First_
  
> [in] Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

La macro **CheckParameters** a été remplacée par la macro [CheckParms](checkparms.md) . **CheckParms** est recommandé sur toutes les plateformes. 
  

