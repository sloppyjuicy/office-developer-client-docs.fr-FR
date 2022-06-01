---
title: CONTAB_ENTRYID
description: CONTAB_ENTRYID contient l’ID d’entrée du dossier contacts. Cet article décrit ses membres et remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
ms.openlocfilehash: 98d154345bb5bc4752685861c2a64837b3611687
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815911"
---
# <a name="contab_entryid"></a>CONTAB_ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’ID d’entrée du dossier contacts.
  
|Propriété |Valeur |
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
  
> Masque de bits des indicateurs qui fournit des informations décrivant l’objet. Pour plus d’informations, consultez la description du champ **abFlags** d’une structure [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID qui identifie le fournisseur du magasin.
    
 **ulVersion**
  
> Numéro de version de la structure **CONTAB_ENTRYID** . Doit être défini sur CONTAB_VERSION. 
    
 **ulType**
  
> Entier représentant le type d’ID d’entrée de contact. Il doit s’agir de l’une des valeurs suivantes :
    
|**Name**|**Description**|
|:-----|:-----|
|CONTAB_USER  <br/> |Objet d’utilisateur de messagerie. |
|CONTAB_DISTLIST  <br/> |Un objet de liste de distribution. |
   
 **ulIndex**
  
> Index dans le sous-ensemble de propriétés d’e-mail.
    
 **cbeid**
  
> Taille de l’identificateur d’entrée du message de contact associé à cette entrée dans le carnet d’adresses des contacts.
    
 **abeid**
  
> Identificateur d’entrée du message de contact associé à cette entrée dans le carnet d’adresses des contacts.
    
## <a name="remarks"></a>Remarques

Un carnet d’adresses de contacts est un carnet d’adresses qui contient tous les éléments de contact d’un dossier Contacts qui ont une adresse e-mail ou un numéro de télécopie. Chaque entrée d’un carnet d’adresses de contacts est associée à une adresse e-mail ou à un numéro de télécopie. Étant donné qu’un élément de contact peut avoir jusqu’à trois adresses e-mail et trois numéros de télécopie, un élément de contact peut être représenté par jusqu’à six entrées dans le carnet d’adresses des contacts correspondant.
  
L’objectif d’un carnet d’adresses de contacts est de prendre en charge les utilisateurs qui traitent des messages électroniques à des contacts dans un dossier Contacts. Le fournisseur de carnets d’adresses de contacts qui Microsoft Outlook 2010 et Microsoft Outlook 2013 prise en charge est contab32.dll.
  
La structure **CONTAB_ENTRYID** prend en charge un sous-ensemble des informations présentes dans le message de contact MAPI sous-jacent. Il identifie le message de contact auquel une entrée de carnet d’adresses de contacts particulière est associée. 
  
Les champs **cbeid** et **abeid** sont valides uniquement lorsque la valeur du champ **ulType** est définie sur CONTAB_DISTLIST ou CONTAB_USER. Lorsque la valeur du champ **ulType** est définie sur CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, la structure [DIR_ENTRYID](dir_entryid.md) doit être utilisée à la place. 
  
## <a name="see-also"></a>Voir aussi



[DIR_ENTRYID](dir_entryid.md)


[Structures MAPI](mapi-structures.md)

