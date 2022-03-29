---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: Décrit une propriété nommée utilisée avec un formulaire pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 1583e318c8dcc42ce0363b8859d4255f036cb918
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454536"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété nommée utilisée avec un formulaire. 
  
|Propriété |Valeur |
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
  
> Indicateurs utilisés pour distinguer le format des chaînes dans la structure **SMAPIFormProp** . L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **nPropType**
  
> Type de la propriété nommée, avec le mot le plus significatif à zéro. 
    
 **nmid**
  
> Nom de la propriété nommée, qui inclut une structure **GUID** identifiant le jeu de propriétés et une valeur numérique ou de chaîne qui représente un identificateur d’interface et un nom de formulaire. 
    
 **pszDisplayName**
  
> Pointeur vers le nom complet de la propriété nommée.
    
 **nSpecialType**
  
> Valeur décrivant le type de données incluses dans le **membre u** . Les valeurs possibles sont les suivantes : 
    
FPST_VANILLA 
  
> Le **membre u** ne contient pas d’éumération. 
    
FPST_ENUM_PROP 
  
> Le **membre u** contient une structure qui décrit une éumération. 
    
 **u**
  
> Union décrivant l’association entre le nom et le numéro de la propriété nommée. À l’aide de certaines propriétés, le **membre u** est vide. Avec d’autres propriétés, elle est représentée dans une structure composée des membres suivants : 
    
 **nmidIdx**
  
> Structure [MAPINAMEID](mapinameid.md) qui contient le jeu de propriétés et l’identificateur de la propriété nommée. 
    
 **cfpevAvailable**
  
> Nombre de structures [SMAPIFormPropEnumVal](smapiformpropenumval.md) dans le tableau pointés par **le membre pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Pointeur vers un tableau de structures **SMAPIFormPropEnumVal** , chacune d’elles contient une valeur pour la propriété nommée. 
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormProp** contient des informations sur une propriété de formulaire utilisée dans le cadre des définitions de l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contient une balise qui s’applique à l’union **u** qui fait partie de **SMAPIFormProp**.
  
## <a name="see-also"></a>Voir aussi



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Structures MAPI](mapi-structures.md)

