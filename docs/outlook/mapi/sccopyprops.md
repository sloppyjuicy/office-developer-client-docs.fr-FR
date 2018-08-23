---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eb3b3b3c9c2e9cffb77febf9c96baed40ce3f9e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566221"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Copie les propriétés définies par un tableau de structures [SPropValue](spropvalue.md) vers un nouvel emplacement. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Paramètres

 _cprop_
  
> [in] Nombre de propriétés à copier. 
    
 _rgprop_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à copier. Le paramètre _rgprop_ ne doit pas pointer vers le début du tableau, mais il doit pointer vers le début d’une des structures **SPropValue** dans le tableau. 
    
 _pvDst_
  
> [in] Pointeur vers la position initiale dans la mémoire à laquelle cette fonction copie les propriétés. 
    
 _carte de circuit imprimé_
  
> [out] Pointeur facultatif à la taille, en octets, du bloc de mémoire vers laquelle pointé le paramètre _pvDst_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Les propriétés ont été copiées avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Un type de propriété inconnue s’est produite.
    
## <a name="remarks"></a>Remarques

Le nouveau tableau et ses données résident dans une mémoire tampon créée en une seule fois, et la fonction [ScRelocProps](screlocprops.md) peut être utilisée pour ajuster les pointeurs dans les structures [SPropValue](spropvalue.md) individuels. Avant cet ajustement, les pointeurs sont valides. 
  
 **ScCopyProps** conserve l’ordre des propriétés d’origine du tableau de propriétés copiées. 
  
Le paramètre de la _carte de circuits imprimés_ est facultatif ; s’il n’est pas NULL, elle est définie pour le nombre d’octets stocké dans le paramètre _pvDst_ . 
  
## <a name="see-also"></a>Voir aussi



[ScDupPropset](scduppropset.md)

