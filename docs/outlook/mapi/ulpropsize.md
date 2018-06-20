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
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787397"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**S’applique à**: Outlook 
  
Retourne la taille d’une seule valeur de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValue_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définit la propriété à mesurer. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

La fonction **UlPropSize** retourne la taille, en octets, de la valeur de propriété pour la propriété spécifiée. Elle ignore la taille du reste de la structure **SPropValue** . 
  

