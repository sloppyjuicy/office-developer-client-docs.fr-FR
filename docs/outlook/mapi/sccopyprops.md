---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9f4b69c62f78805e93f28db73691830515997fa3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586788"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie les propriétés définies par un tableau de structures [SPropValue](spropvalue.md) vers une nouvelle destination. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à copier. Le  _paramètre rgprop_ n’a pas besoin de pointer vers le début du tableau, mais il doit pointer vers le début de l’une des structures **SPropValue** dans le tableau. 
    
 _pvDst_
  
> [in] Pointeur vers la position initiale de la mémoire vers laquelle cette fonction copie les propriétés. 
    
 _pcb_
  
> [out] Pointeur facultatif vers la taille, en octets, du bloc de mémoire pointé par le _paramètre pvDst._ 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les propriétés ont été correctement copiées.
    
MAPI_E_INVALID_PARAMETER
  
> Un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

Le nouveau tableau et ses données résident dans une mémoire tampon créée avec une allocation unique, et la fonction [ScRelocProps](screlocprops.md) peut être utilisée pour ajuster les pointeurs dans les structures [SPropValue](spropvalue.md) individuelles. Avant cet ajustement, les pointeurs sont valides. 
  
 **ScCopyProps** conserve l’ordre des propriétés d’origine pour le tableau de propriétés copiées. 
  
Le _paramètre pcb_ est facultatif ; si elle n’est pas NULL, elle est définie sur le nombre d’octets stockés dans le _paramètre pvDst._ 
  
## <a name="see-also"></a>Voir aussi



[ScDupPropset](scduppropset.md)

