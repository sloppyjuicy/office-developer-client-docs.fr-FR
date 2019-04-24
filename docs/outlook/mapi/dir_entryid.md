---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316673"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les propriétés d'un ID d'entrée d'annuaire.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |EntryID. h  <br/> |
   
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
  
> Masque de des indicateurs qui fournit des informations décrivant l'objet. Pour plus d'informations, reportez-vous à la description du champ **abFlags** d'une structure [EntryID](entryid.md) . 
    
 **muid**
  
> GUID qui identifie le fournisseur de banque.
    
 **ulVersion**
  
> Numéro de version de la structure **DIR_ENTRYID** . Doit être défini sur CONTAB_VERSION. 
    
 **ulType**
  
> Entier représentant le type d'ID d'entrée d'annuaire. Il doit prendre la valeur de l'une des valeurs suivantes:
    
|**Nom**|**Description**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Dossier racine d'un carnet d'adresses MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Sous-dossier inclus dans le dossier racine de l’objet de carnet d’adresses MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Un objet conteneur de carnet d'adresses.  <br/> |
   
 **muidID**
  
> GUID qui identifie l'objet d'ouverture de session.
    
## <a name="remarks"></a>Remarques

Les structures **DIR_ENTRYID** et [CONTAB_ENTRYID](contab_entryid.md) sont identiques, à l'exception du membre **ulType** . Le contenu du membre **ulType** détermine la structure appropriée pour les champs restants. 
  
## <a name="see-also"></a>Voir aussi



[CONTAB_ENTRYID](contab_entryid.md)


[Structures MAPI](mapi-structures.md)

