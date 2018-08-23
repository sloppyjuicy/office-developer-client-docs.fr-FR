---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582034"
---
# <a name="checkparms"></a>CheckParms

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de service appelées par MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par l’énumération, la méthode à valider. 
    
 _Premier_
  
> [in] Pointeur vers le premier argument dans la pile.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Contrairement aux [ValidateParms](validateparms.md) et [UlValidateParms](ulvalidateparms.md) des macros, la macro **CheckParms** n’effectue pas une validation de paramètre complet. Paramètres passés entre MAPI et service fournisseurs sont supposés soit correct **CheckParms** effectue une validation de débogage uniquement. 
  

