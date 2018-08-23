---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583343"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit les propriétés de l’id d’entrée de répertoire.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |EntryID.h  <br/> |
   
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
  
> GUID qui identifie le fournisseur de banque.
    
 **ulVersion**
  
> Le numéro de version de la structure **DIR_ENTRYID** . Doit être défini sur CONTAB_VERSION. 
    
 **ulType**
  
> Nombre entier représentant le type d’ID de l’entrée directory. Il doit être une des valeurs suivantes :
    
|**Nom**|**Description**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Le dossier racine d’un carnet d’adresses MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Un sous-dossier contenu dans le dossier racine de l’objet de carnet d’adresses MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Un objet conteneur de carnet d'adresses.  <br/> |
   
 **muidID**
  
> GUID qui identifie l’objet d’ouverture de session.
    
## <a name="remarks"></a>Remarques

Les structures **DIR_ENTRYID** et [CONTAB_ENTRYID](contab_entryid.md) sont identiques, à l’exception du membre **ulType** . Le contenu du membre **ulType** détermine dont la structure est appropriée pour les champs restants. 
  
## <a name="see-also"></a>Voir aussi



[CONTAB_ENTRYID](contab_entryid.md)


[Structures MAPI](mapi-structures.md)

