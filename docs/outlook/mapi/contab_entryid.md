---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424083"
---
# <a name="contab_entryid"></a>CONTAB_ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’ID d’entrée du dossier contacts.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |msomapiutil.h  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a>Members

 **abFlags**
  
> Masque de bits d’indicateurs qui fournit des informations décrivant l’objet. Pour plus d’informations, voir la description du champ **abFlags** d’une structure [ENTRYID.](entryid.md) 
    
 **muid**
  
> GUID qui identifie le fournisseur du magasin.
    
 **ulVersion**
  
> Numéro de version de la structure **CONTAB_ENTRYID** de base. Doit être définie sur CONTAB_VERSION. 
    
 **ulType**
  
> Unteger représentant le type d’ID d’entrée de contact. Elle doit avoir l’une des valeurs suivantes :
    
|**Name**|**Description**|
|:-----|:-----|
|CONTAB_USER  <br/> |Objet d’utilisateur de messagerie.  <br/> |
|CONTAB_DISTLIST  <br/> |Un objet de liste de distribution.  <br/> |
   
 **ulIndex**
  
> Index dans le sous-ensemble de propriétés de messagerie.
    
 **cbeid**
  
> Taille de l’identificateur d’entrée du message contact associé à cette entrée dans le carnet d’adresses des contacts.
    
 **abeid**
  
> Identificateur d’entrée du message contact associé à cette entrée dans le carnet d’adresses des contacts.
    
## <a name="remarks"></a>Remarques

Un carnet d’adresses de contacts est un carnet d’adresses qui contient tous les éléments de contact d’un dossier Contacts qui ont une adresse de messagerie ou un numéro de télécopie. Chaque entrée d’un carnet d’adresses de contacts est associée à une adresse de messagerie ou à un numéro de télécopie. Étant donné qu’un élément de contact peut avoir jusqu’à trois adresses de messagerie et trois numéros de télécopie, un élément de contact peut être représenté par six entrées au plus dans le carnet d’adresses des contacts correspondant.
  
L’objectif d’un carnet d’adresses de contacts est de prendre en charge les utilisateurs qui adressent des messages électroniques à des contacts dans un dossier Contacts. Le fournisseur de carnet d’adresses contacts que Microsoft Outlook 2010 et Microsoft Outlook 2013 prendre en charge est contab32.dll.
  
La **structure CONTAB_ENTRYID** prend en charge un sous-ensemble des informations présentes dans le message de contact MAPI sous-jacent. Il identifie le message de contact associé à une entrée de carnet d’adresses de contacts particulière. 
  
Les **champs cbeid** et **abeid** ne sont valides que lorsque la valeur du champ **ulType** est définie sur CONTAB_DISTLIST ou CONTAB_USER. Lorsque la valeur du champ **ulType** est définie sur CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, la [structure](dir_entryid.md) DIR_ENTRYID doit être utilisée à la place. 
  
## <a name="see-also"></a>Voir aussi



[DIR_ENTRYID](dir_entryid.md)


[Structures MAPI](mapi-structures.md)

