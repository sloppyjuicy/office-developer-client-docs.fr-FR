---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416698"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété nommée utilisée avec un formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> Indicateurs utilisés pour distinguer le format des chaînes dans la structure **SMAPIFormProp.** L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **nPropType**
  
> Type de la propriété nommée, avec le mot le plus significatif à zéro. 
    
 **nmid**
  
> Nom de la propriété nommée, qui inclut une structure **GUID** identifiant le jeu de propriétés et une valeur numérique ou de chaîne qui représente un identificateur d’interface et un nom de formulaire. 
    
 **pszDisplayName**
  
> Pointeur vers le nom complet de la propriété nommée.
    
 **nSpecialType**
  
> Valeur décrivant le type de données incluses dans le **membre u.** Les valeurs possibles sont les suivantes : 
    
FPST_VANILLA 
  
> Le **membre u** ne contient pas d’éumération. 
    
FPST_ENUM_PROP 
  
> Le **membre u** contient une structure qui décrit une éumération. 
    
 **u**
  
> Union décrivant l’association entre le nom et le numéro de la propriété nommée. À l’aide de certaines propriétés, le **membre u** est vide. Avec d’autres propriétés, elle est représentée dans une structure composée des membres suivants : 
    
 **nmidIdx**
  
> Structure [MAPINAMEID](mapinameid.md) qui contient le jeu de propriétés et l’identificateur de la propriété nommée. 
    
 **cfpevAvailable**
  
> Nombre de structures [SMAPIFormPropEnumVal](smapiformpropenumval.md) dans le tableau pointés par **le membre pfpevAvailable.** 
    
 **pfpevAvailable**
  
> Pointeur vers un tableau de structures **SMAPIFormPropEnumVal,** chacune d’elles contient une valeur pour la propriété nommée. 
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormProp** contient des informations sur une propriété de formulaire utilisée dans le cadre des définitions de l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType contient** une balise qui s’applique à l’union **u** qui fait partie de **SMAPIFormProp**.
  
## <a name="see-also"></a>Voir aussi



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Structures MAPI](mapi-structures.md)

