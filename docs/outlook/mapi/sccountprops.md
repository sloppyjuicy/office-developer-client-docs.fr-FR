---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Détermine la taille, en octets, d’un tableau de valeurs de propriétés et valide la mémoire associée au tableau. '
ms.openlocfilehash: 4758db12b682ba49afbb6f64e06d0183b5083b2d
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764187"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la taille, en octets, d’un tableau de valeurs de propriétés et valide la mémoire associée au tableau. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cprop_
  
> [in] Nombre de propriétés dans le tableau indiqué par le  _paramètre rgprop_ . 
    
 _rgprop_
  
> [in] Pointeur vers une plage dans un tableau de structures [SPropValue](spropvalue.md) qui définit les propriétés dont la taille doit être déterminée. Cette plage ne commence pas nécessairement au début du tableau. 
    
 _pcb_
  
> [out] Pointeur facultatif vers la taille, en octets, du tableau de propriétés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_INVALID_PARAMETER 
  
> Au moins une propriété du tableau de valeurs de propriétés possède un identificateur PROP_ID_NULL ou PROP_ID_INVALID, ou le tableau de propriétés contient une propriété à valeurs multiples sans valeur de propriété.
    
## <a name="remarks"></a>Remarques

Si NULL est transmis dans le _paramètre pcb_ , la **fonction ScCountProps** valide le tableau de notifications, mais aucun décompte n’est effectué. Si une valeur non null est passée dans  _pcb_, la **fonction ScCountNotifications** détermine la taille du tableau et stocke la  _cause pcb_. Le  _paramètre pcb_ doit être suffisamment grand pour contenir la totalité du tableau. 
  
Au cours de son comptage, **ScCountProps** valide la mémoire associée au tableau. **ScCountProps fonctionne** uniquement avec les propriétés sur lesquelles MAPI dispose d’informations. 
  
## <a name="see-also"></a>Voir aussi



[PropCopyMore](propcopymore.md)

