---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7f7a35716c37228c3c113c99739fd3b4c8f798e0
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784285"
---
# <a name="dir_entryid"></a>DIR_ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les propriétés d’un ID d’entrée d’annuaire.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |entryid.h  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a>Members

 **abFlags**
  
> Masque de bits d’indicateurs qui fournit des informations décrivant l’objet. Pour plus d’informations, voir la description du champ **abFlags** d’une structure [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID qui identifie le fournisseur du magasin.
    
 **ulVersion**
  
> Numéro de version de la structure **DIR_ENTRYID** de base. Doit être définie sur CONTAB_VERSION. 
    
 **ulType**
  
> Un integer représentant le type d’ID d’entrée d’annuaire. Elle doit avoir l’une des valeurs suivantes :
    
|**Name**|**Description**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Dossier racine d’un carnet d’adresses MAPI. |
|CONTAB_SUBROOT  <br/> |Sous-dossier inclus dans le dossier racine de l’objet de carnet d’adresses MAPI. |
|CONTAB_CONTAINER  <br/> |Un objet conteneur de carnet d'adresses. |
   
 **muidID**
  
> GUID qui identifie l’objet d’identification.
    
## <a name="remarks"></a>Remarques

Les structures **DIR_ENTRYID** et [CONTAB_ENTRYID](contab_entryid.md) sont identiques, à l’exception du **membre ulType** . Le contenu du membre **ulType** détermine la structure appropriée pour les champs restants. 
  
## <a name="see-also"></a>Voir aussi



[CONTAB_ENTRYID](contab_entryid.md)


[Structures MAPI](mapi-structures.md)

