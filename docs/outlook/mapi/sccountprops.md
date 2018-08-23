---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583350"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Détermine la taille, en octets, d’un tableau de valeurs de propriété et valide la mémoire associée au tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cprop_
  
> [in] Nombre de propriétés dans le tableau indiqué par le paramètre _rgprop_ . 
    
 _rgprop_
  
> [in] Pointeur vers une plage dans un tableau de structures [SPropValue](spropvalue.md) qui définit les propriétés dont la taille est déterminée. Cette plage ne démarre pas nécessairement au début du tableau. 
    
 _carte de circuit imprimé_
  
> [out] Pointeur facultatif à la taille, en octets, du tableau de la propriété.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_INVALID_PARAMETER 
  
> Au moins une propriété dans le tableau de valeurs de propriété est un identificateur de PROP_ID_NULL ou PROP_ID_INVALID, ou le tableau de propriétés contient une propriété à valeurs multiples avec aucune valeur de propriété.
    
## <a name="remarks"></a>Remarques

Si NULL est indiqué dans le paramètre de la _carte de circuit imprimé_ , la fonction **ScCountProps** valide le tableau des notifications, mais aucun décompte n’effectué. Si une valeur non nulle est passée dans une _carte de circuit imprimé_, la fonction **ScCountNotifications** détermine la taille du tableau et stocke la cause la _carte de circuit imprimé_. Le paramètre de la _carte de circuit imprimé_ doit être suffisant pour contenir l’intégralité du tableau. 
  
Comme il est compté, **ScCountProps** valide la mémoire associée au tableau. **ScCountProps** fonctionne uniquement avec les propriétés comporte des informations sur les MAPI. 
  
## <a name="see-also"></a>Voir aussi



[PropCopyMore](propcopymore.md)

