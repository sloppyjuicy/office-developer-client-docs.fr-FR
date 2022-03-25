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
description: Copie les propriétés définies par un tableau de structures SPropValue vers une nouvelle destination.  ScCopyProps conserve l’ordre des propriétés d’origine pour le tableau de propriétés copiées.
ms.openlocfilehash: 805784f51fc0ed3b461152bc644579a9da8b7202
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762087"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie les propriétés définies par un tableau de structures [SPropValue](spropvalue.md) vers une nouvelle destination. 
  
|Propriété |Valeur |
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
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à copier. Le  _paramètre rgprop_ ne doit pas pointer vers le début du tableau, mais il doit pointer vers le début de l’une des structures **SPropValue** dans le tableau. 
    
 _pvDst_
  
> [in] Pointeur vers la position initiale de la mémoire vers laquelle cette fonction copie les propriétés. 
    
 _pcb_
  
> [out] Pointeur facultatif vers la taille, en octets, du bloc de mémoire pointé par le  _paramètre pvDst_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les propriétés ont été copiées avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

Le nouveau tableau et ses données résident dans une mémoire tampon créée avec une allocation unique, et la fonction [ScRelocProps](screlocprops.md) peut être utilisée pour ajuster les pointeurs dans les structures [SPropValue](spropvalue.md) individuelles. Avant cet ajustement, les pointeurs sont valides. 
  
 **ScCopyProps** conserve l’ordre des propriétés d’origine pour le tableau de propriétés copiées. 
  
Le  _paramètre pcb_ est facultatif ; si elle n’est pas NULL, elle est définie sur le nombre d’octets stockés dans le _paramètre pvDst_ . 
  
## <a name="see-also"></a>Voir aussi



[ScDupPropset](scduppropset.md)

