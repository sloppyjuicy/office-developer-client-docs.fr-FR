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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 73475c5ee4e715796e06642756c05746b271d128
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787192"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**S’applique à**: Outlook 
  
Décrit une propriété nommée est utilisée avec un formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
   
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
  
> Indicateurs permet de distinguer le format des chaînes dans la structure **SMAPIFormProp** . Vous pouvez définir l’indicateur suivant : 
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **nPropType**
  
> Type de la propriété nommée, avec le mot plus importante définir sur zéro. 
    
 **nmid**
  
> Nom de la propriété nommée, qui inclut une structure **GUID** qui identifie la valeur de propriété set et un numérique ou chaîne qui représente un nom de formulaire et d’identificateur d’interface. 
    
 **pszDisplayName**
  
> Pointeur vers le nom complet de la propriété nommée.
    
 **nSpecialType**
  
> Valeur décrivant le type de données inclus dans le membre **u** . Les valeurs possibles sont les suivantes : 
    
FPST_VANILLA 
  
> Le membre **u** ne contient pas une énumération. 
    
FPST_ENUM_PROP 
  
> Le membre **u** contient une structure qui décrit une énumération. 
    
 **u**
  
> Union décrivant l’association entre le nom et le numéro de la propriété nommée. À l’aide de certaines propriétés, le membre **u** est vide. Avec d’autres propriétés, il est représenté dans une structure composée des membres suivants : 
    
 **nmidIdx**
  
> La structure [MAPINAMEID](mapinameid.md) qui contient le jeu de propriétés et l’identificateur de la propriété nommée. 
    
 **cfpevAvailable**
  
> Nombre de structures [SMAPIFormPropEnumVal](smapiformpropenumval.md) dans le tableau indiqué par le membre **pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Pointeur vers un tableau de structures **SMAPIFormPropEnumVal** , chacun d'entre eux conserve une valeur pour la propriété nommée. 
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormProp** contient des informations sur une propriété de formulaire utilisée dans le cadre des définitions de l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contient une balise qui s’applique à l’union **u** qui fait partie de **SMAPIFormProp**.
  
## <a name="see-also"></a>Voir aussi



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Structures MAPI](mapi-structures.md)

