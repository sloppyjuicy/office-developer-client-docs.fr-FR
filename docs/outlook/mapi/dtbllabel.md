---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783233"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**S’applique à**: Outlook 
  
Décrit une étiquette qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Membres

 **ulbLpszLabelName**
  
> Position dans la mémoire de l’étiquette de chaîne de caractères.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabelName** . Vous pouvez définir l’indicateur suivant : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLLABEL** décrit un texte de contrôle d’étiquette qui s’affiche avec un autre type de contrôle à ajouter la signification de ce contrôle. Par exemple, la plupart des contrôles d’édition sont positionnés en regard des étiquettes pour informer l’utilisateur à entrer le type d’informations. Certains contrôles, tels que les zones de groupe et de cases d’option, maintenez la touche leurs propres étiquettes. 
  
L’étiquette peut inclure un raccourci Windows, identifiée comme le caractère qui suit le signe (&amp;). Appuyer sur la touche d’accès rapide place le focus dans la première nonlabel, contrôle libellés suivant cette étiquette dans le tableau d’affichage.
  
Il n’existe aucune prise en charge pour les étiquettes multilignes. Afficher plusieurs lignes nécessite plusieurs étiquettes.
  
Il n’est pas possible d’utiliser une étiquette comme un contrôle d’édition en lecture seule. La différence est qu’un contrôle d’édition peut être sélectionné et copié qu’une étiquette ne peut pas. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

