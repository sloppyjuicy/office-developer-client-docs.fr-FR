---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421584"
---
# <a name="guid"></a>GUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un identificateur global unique (GUID). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiguid. h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

 **Data1**
  
> Valeur de type long Integer non signée.
    
 **Data2**
  
> Valeur de type Integer courte non signée.
    
 **Data3**
  
> Valeur de type Integer courte non signée.
    
 **Data4**
  
> Tableau de caractères non signés.
    
## <a name="remarks"></a>Remarques

 Les structures de **GUID** sont utilisées dans MAPI de la manière suivante: 
  
- Dans les structures [MAPIUID](mapiuid.md) qui identifient les fournisseurs de services de manière unique. 
    
- Pour les identificateurs d'interface.
    
- Dans le jeu de propriétés, définissez les noms des propriétés nommées. 
    
Banque de messages et fournisseurs de carnet d'adresses génèrent une structure de **GUID** à utiliser dans leur structure **MAPIUID** . En transmettant le **MAPIUID** résultant à [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md), ces fournisseurs de services informent MAPI de leur identificateur unique.
  
En outre, elles sont utilisées dans l'implémentation de l'appel de procédure disTante (RPC) Microsoft et du langage ODL (Object Description Language). Pour plus d'informations sur ces utilisations ** , reportez-vous au *Guide de référence du programmeur RPC Microsoft et*à l' *intérieur OLE*, *deuxième édition* . 
  
La structure du **GUID** est définie dans le *Guide de référence du programmeur Win32* . Les valeurs spécifiques des structures de **GUID** utilisées dans MAPI sont définies dans le fichier d'en-tête MAPI Mapiguid. h. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)


[Structures MAPI](mapi-structures.md)

