---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421087"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajuste les pointeurs dans un tableau [SPropValue](spropvalue.md) après que le tableau et ses données ont été copiés ou déplacés vers un nouvel emplacement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cprop_
  
> dans Nombre de propriétés dans le tableau vers lequel pointe le paramètre _rgprop_ . 
    
 _rgprop_
  
> dans Pointeur vers un tableau de structures [SPropValue](spropvalue.md) pour lesquelles les pointeurs doivent être ajustés. 
    
 _pvBaseOld_
  
> dans Pointeur vers l'adresse de base d'origine du tableau vers lequel pointe le paramètre _rgprop_ . 
    
 _pvBaseNew_
  
> dans Pointeur vers la nouvelle adresse de base du tableau désigné par le paramètre _rgprop_ . 
    
 _circuits_
  
> [in, out] Pointeur facultatif vers la taille, en octets, du tableau indiqué par le paramètre _pvBaseNew_ . Si la valeur n'est pas NULL, le paramètre _PCB_ est défini sur le nombre d'octets stockés dans le paramètre _pvD_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les pointeurs ont été ajustés avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Un ou les deux paramètres n'étaient pas valides ou un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

La fonction **ScRelocProps** agit sur l'hypothèse que le tableau de valeurs de propriété pour lequel les pointeurs sont ajustés a été alloué à l'origine dans un appel unique semblable à un appel à la fonction **ScCopyProps** . Si une application cliente ou un fournisseur de services travaille avec une valeur de propriété qui est générée à partir de blocs de mémoire disjoints, elle doit utiliser [ScCopyProps](sccopyprops.md) pour copier les propriétés. 
  
 **ScRelocProps** est utilisé pour maintenir la validité des pointeurs dans un tableau [SPropValue](spropvalue.md) . Pour maintenir la validité des pointeurs lors de l'écriture et de la lecture d'un tel tableau sur un disque, effectuez les opérations suivantes: 
  
1. Avant d'écrire le tableau et les données sur un disque, appelez **ScRelocProps** sur le tableau avec le paramètre _pvBaseNew_ pointant vers un zéro de valeur standard, par exemple. 
    
2. Après avoir lu le tableau et les données à partir d'un disque, appelez **ScRelocProps** sur le tableau avec le paramètre _pvBaseOld_ égal à la même valeur standard utilisée à l'étape 1. Le tableau et les données doivent être lus dans une mémoire tampon créée avec une seule allocation. 
    
3. Le paramètre _PCB_ vers **ScRelocProps** est facultatif. 
    
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

