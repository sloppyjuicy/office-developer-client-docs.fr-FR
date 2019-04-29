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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411007"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie les propriétés définies par un tableau de structures [SPropValue](spropvalue.md) vers une nouvelle destination. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Nombre de propriétés à copier. 
    
 _rgprop_
  
> dans Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à copier. Le paramètre _rgprop_ n'a pas besoin de pointer vers le début du tableau, mais il doit pointer vers le début de l'une des structures **SPropValue** dans le tableau. 
    
 _pvDst_
  
> dans Pointeur vers la position initiale dans la mémoire à laquelle cette fonction copie les propriétés. 
    
 _circuits_
  
> remarquer Pointeur facultatif vers la taille, en octets, du bloc de mémoire pointé par le paramètre _pvDst_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les propriétés ont été correctement copiées.
    
MAPI_E_INVALID_PARAMETER
  
> Un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

Le nouveau tableau et ses données résident dans une mémoire tampon créée avec une seule allocation, et la fonction [ScRelocProps](screlocprops.md) peut être utilisée pour ajuster les pointeurs dans les structures [SPropValue](spropvalue.md) individuelles. Avant ce réglage, les pointeurs sont valides. 
  
 **ScCopyProps** conserve l'ordre des propriétés d'origine pour le tableau de propriétés copié. 
  
Le paramètre _PCB_ est facultatif; Si ce n'est pas le cas, la valeur est définie sur le nombre d'octets stockés dans le paramètre _pvDst_ . 
  
## <a name="see-also"></a>Voir aussi



[ScDupPropset](scduppropset.md)

