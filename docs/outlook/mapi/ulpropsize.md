---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: Renvoie la taille d’une valeur de propriété unique. La fonction ignore la taille du reste de la structure SPropValue.
ms.openlocfilehash: 4015771f3a579d527b268e376a9d151685d4844e
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406259"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie la taille d’une valeur de propriété unique. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValue_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la propriété à mesurer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération.
    
## <a name="remarks"></a>Remarques

La **fonction UlPropSize** renvoie la taille, en octets, de la valeur de la propriété spécifiée. Il ignore la taille du reste de la structure **SPropValue** . 
  

