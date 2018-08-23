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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 241fac608552036e4706956cbe79524aaedacec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576847"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ajuster les pointeurs dans un tableau [SPropValue](spropvalue.md) après que le tableau et ses données ont été copiés ou déplacés vers un nouvel emplacement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Nombre de propriétés dans le tableau indiqué par le paramètre _rgprop_ . 
    
 _rgprop_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) pour lequel des pointeurs doivent être ajustés. 
    
 _pvBaseOld_
  
> [in] Pointeur vers l’adresse de base d’origine du tableau indiqué par le paramètre _rgprop_ . 
    
 _pvBaseNew_
  
> [in] Pointeur vers la nouvelle adresse de base du tableau indiqué par le paramètre _rgprop_ . 
    
 _carte de circuit imprimé_
  
> [entrée, sortie] Pointeur facultatif à la taille, en octets, du tableau indiquée par le paramètre _pvBaseNew_ . Si ce n’est pas NULL, le paramètre de la _carte de circuits imprimés_ est défini sur le nombre d’octets stocké dans le paramètre _pvD_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Pointeurs ont été ajustés avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Un ou les deux paramètres ne sont pas valides, ou un type de propriété inconnue s’est produite.
    
## <a name="remarks"></a>Remarques

La fonction **ScRelocProps** fonctionne sur l’hypothèse que le tableau de valeurs de propriété pour laquelle des pointeurs sont ajustées alloué initialement en un seul appel semblable à un appel à la fonction **ScCopyProps** . Si une application cliente ou un fournisseur de services fonctionne avec une valeur de propriété qui est générée à partir des blocs de mémoire, il doit utiliser [ScCopyProps](sccopyprops.md) pour copier les propriétés. 
  
 **ScRelocProps** est utilisée pour mettre à jour de la validité des pointeurs dans un tableau [SPropValue](spropvalue.md) . Pour maintenir la validité des pointeurs lorsque vous écrivez de ce type de tableau à et lire à partir d’un disque, effectuez les opérations suivantes : 
  
1. Avant d’écrire le tableau et les données sur un disque, appelez **ScRelocProps** dans le tableau avec le paramètre _pvBaseNew_ pointe vers une valeur standard zéro, par exemple. 
    
2. Après avoir lu le tableau et les données d’un disque, appelez **ScRelocProps** dans le tableau avec le paramètre _pvBaseOld_ égale à la même valeur standard utilisée à l’étape 1. Le tableau et les données doivent être lus dans un tampon créé en une seule fois. 
    
3. Le paramètre de la _carte de circuit imprimé_ à **ScRelocProps** est facultatif. 
    
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

