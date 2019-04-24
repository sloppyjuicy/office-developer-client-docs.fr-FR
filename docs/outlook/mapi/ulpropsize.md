---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315301"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la taille d'une seule valeur de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValue_
  
> dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la propriété à mesurer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.
    
## <a name="remarks"></a>Remarques

La fonction **UlPropSize** renvoie la taille en octets de la valeur de la propriété spécifiée. Il ignore la taille du reste de la structure **SPropValue** . 
  

