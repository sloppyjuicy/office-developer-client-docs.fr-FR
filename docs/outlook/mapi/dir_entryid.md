---
title: DIR_ENTRYID
description: DIR_ENTRYID décrit les propriétés d’un ID d’entrée de répertoire. Cet article décrit ses membres et remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
ms.openlocfilehash: b67ee874a4916b28ef532f8da5755d1ccbb77fc9
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817115"
---
# <a name="dir_entryid"></a>DIR_ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les propriétés d’un ID d’entrée de répertoire.
  
|Propriété |Valeur |
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
  
> Masque de bits des indicateurs qui fournit des informations décrivant l’objet. Pour plus d’informations, consultez la description du champ **abFlags** d’une structure [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID qui identifie le fournisseur du magasin.
    
 **ulVersion**
  
> Numéro de version de la structure **DIR_ENTRYID** . Doit être défini sur CONTAB_VERSION. 
    
 **ulType**
  
> Entier représentant le type d’ID d’entrée de répertoire. Il doit s’agir de l’une des valeurs suivantes :
    
|**Name**|**Description**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Dossier racine d’un carnet d’adresses MAPI. |
|CONTAB_SUBROOT  <br/> |Sous-dossier inclus dans le dossier racine de l’objet de carnet d’adresses MAPI. |
|CONTAB_CONTAINER  <br/> |Un objet conteneur de carnet d'adresses. |
   
 **muidID**
  
> GUID qui identifie l’objet d’ouverture de session.
    
## <a name="remarks"></a>Remarques

Les structures **DIR_ENTRYID** et [CONTAB_ENTRYID](contab_entryid.md) sont identiques, à l’exception du membre **ulType** . Le contenu du membre **ulType** détermine la structure appropriée pour les champs restants. 
  
## <a name="see-also"></a>Voir aussi



[CONTAB_ENTRYID](contab_entryid.md)


[Structures MAPI](mapi-structures.md)

