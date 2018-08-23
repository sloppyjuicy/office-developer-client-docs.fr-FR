---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567152"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée du dossier contacts.
  
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
  
> Masque de bits d’indicateurs qui fournit des informations décrivant l’objet. Pour plus d’informations, voir la description du champ **abFlags** d’une structure [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID qui identifie le fournisseur de banque.
    
 **ulVersion**
  
> Le numéro de version de la structure **CONTAB_ENTRYID** . Doit être défini sur CONTAB_VERSION. 
    
 **ulType**
  
> Nombre entier représentant le type d’ID entrée du contact. Il doit être une des valeurs suivantes :
    
|**Nom**|**Description**|
|:-----|:-----|
|CONTAB_USER  <br/> |Un objet utilisateur de messagerie.  <br/> |
|CONTAB_DISTLIST  <br/> |Un objet de liste de distribution.  <br/> |
   
 **ulIndex**
  
> L’index dans le sous-ensemble de propriété de messagerie.
    
 **cbeid**
  
> La taille de l’identificateur d’entrée du message Contact associé à cette entrée dans le carnet d’adresses de Contacts.
    
 **abeid**
  
> L’identificateur d’entrée du message Contact associé à cette entrée dans le carnet d’adresses de Contacts.
    
## <a name="remarks"></a>Remarques

Un carnet d’adresses de Contacts est un carnet d’adresses qui contient tous les éléments Contacts dans un dossier Contacts qui possèdent une adresse de messagerie ou un numéro de télécopie. Chaque entrée dans un carnet d’adresses de Contacts est associée à une adresse électronique ou un numéro de télécopie. Dans la mesure où un élément de contact peut avoir jusqu'à trois adresses de messagerie et trois numéros de télécopie, un élément de contact peut être représenté par jusqu'à six entrées dans le carnet d’adresses de Contacts correspondant.
  
L’objectif d’un carnet d’adresses de Contacts consiste à prendre en charge les utilisateurs de l’adressage des messages électroniques aux contacts d’un dossier Contacts. Le fournisseur de carnet d’adresses de Contacts qui prennent en charge de Microsoft Outlook 2010 et Microsoft Outlook 2013 est contab32.dll.
  
La structure **CONTAB_ENTRYID** prend en charge un sous-ensemble des informations qui se trouve dans le message MAPI Contact sous-jacent. Il identifie le message de Contact qui est associée à une entrée de carnet d’adresses de Contacts particulier. 
  
Les champs **cbeid** et **abeid** ne sont valides que lorsque la valeur du champ **ulType** est définie sur CONTAB_DISTLIST ou CONTAB_USER. Lorsque la valeur du champ **ulType** est définie sur CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, la structure [DIR_ENTRYID](dir_entryid.md) doit être utilisée à la place. 
  
## <a name="see-also"></a>Voir aussi



[DIR_ENTRYID](dir_entryid.md)


[Structures MAPI](mapi-structures.md)

