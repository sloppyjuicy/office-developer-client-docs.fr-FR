---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ae3ab19e96aa4c80d6b39bda3ccddc3bcbc01af
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462233"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajuste les pointeurs dans un tableau [SPropValue](spropvalue.md) une fois que le tableau et ses données ont été copiés ou déplacés vers un nouvel emplacement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
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
  
> [in] Nombre de propriétés dans le tableau pointées par le  _paramètre rgprop_ . 
    
 _rgprop_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) pour lesquelles les pointeurs doivent être ajustés. 
    
 _pvBaseOld_
  
> [in] Pointeur vers l’adresse de base d’origine du tableau pointée par le  _paramètre rgprop_ . 
    
 _pvBaseNew_
  
> [in] Pointeur vers la nouvelle adresse de base du tableau pointée par le  _paramètre rgprop_ . 
    
 _pcb_
  
> [in, out] Pointeur facultatif vers la taille, en octets, du tableau indiqué par le  _paramètre pvBaseNew_ . Si la valeur n’est pas NULL, le  _paramètre pcb_ est définie sur le nombre d’octets stockés dans le _paramètre pvD_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les pointeurs ont été correctement ajustés.
    
MAPI_E_INVALID_PARAMETER
  
> Un ou les deux paramètres n’étaient pas valides ou un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

La **fonction ScRelocProps** fonctionne sur l’hypothèse que le tableau de valeurs de propriétés pour lequel les pointeurs sont ajustés a été initialement alloué dans un seul appel semblable à un appel à la fonction **ScCopyProps** . Si une application cliente ou un fournisseur de services utilise une valeur de propriété qui est construite à partir de blocs de mémoire disjoints, il doit utiliser [ScCopyProps](sccopyprops.md) pour copier les propriétés à la place. 
  
 **ScRelocProps est** utilisé pour maintenir la validité des pointeurs dans un tableau [SPropValue](spropvalue.md) . Pour conserver la validité des pointeurs lors de l’écriture et de la lecture d’un tel tableau sur un disque, effectuez les opérations suivantes : 
  
1. Avant d’écrire le tableau et les données sur un disque, appelez **ScRelocProps** sur le tableau avec le paramètre  _pvBaseNew_ pointant vers une valeur standard zéro, par exemple. 
    
2. Après avoir lu le tableau et les données à partir d’un disque, appelez **ScRelocProps** sur le tableau avec le paramètre  _pvBaseOld_ égal à la valeur standard utilisée à l’étape 1. Le tableau et les données doivent être lus dans une mémoire tampon créée avec une allocation unique. 
    
3. Le  _paramètre pcb_ de **ScRelocProps est** facultatif. 
    
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

