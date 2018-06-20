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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783424"
---
# <a name="guid"></a>GUID

  
  
**S’applique à**: Outlook 
  
Décrit un identificateur global unique (GUID). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiguid.h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Membres

 **Data1**
  
> Une valeur de données entier long non signé.
    
 **Data2**
  
> Une valeur de données entier court non signé.
    
 **Data3**
  
> Une valeur de données entier court non signé.
    
 **Données4**
  
> Un tableau de caractères non signés.
    
## <a name="remarks"></a>Remarques

 Structures **GUID** sont utilisés dans MAPI comme suit : 
  
- Dans les structures [MAPIUID](mapiuid.md) qui identifient les fournisseurs de services. 
    
- Pour les identificateurs d’interface.
    
- Dans la propriété définie les noms des propriétés nommées. 
    
Banque de messages et l’adresse génèrent des fournisseurs de carnet d’une structure **GUID** à utiliser dans leur structure **MAPIUID** . En transmettant le résultant **MAPIUID** à [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), ces fournisseurs de services informent MAPI de leur identificateur unique.
  
En outre, ils sont utilisés dans l’implémentation du service d’appel de procédure distante (RPC) Microsoft et de l’objet Description Language (ODL). Pour plus d’informations sur ces utilisations, voir la *référence et le Guide du programmeur Microsoft RPC*, *référence du programmeur OLE* et *à l’intérieur de OLE*, *Deuxième Édition* . 
  
La structure **GUID** est définie dans la *référence du programmeur Win32* . Valeurs spécifiques pour les structures **GUID** qui sont utilisés dans MAPI sont définies dans le fichier d’en-tête Mapiguid.h MAPI. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)


[Structures MAPI](mapi-structures.md)

