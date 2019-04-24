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
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287159"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une étiquette qui sera utilisée dans une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Position en mémoire de l'étiquette de chaîne de caractères.
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format de l'étiquette désignée par le membre **ulbLpszLabelName** . L'indicateur suivant peut être défini: 
    
MAPI_UNICODE 
  
> L'étiquette est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLLABEL** décrit un texte de contrôle d'étiquette qui est affiché avec un autre type de contrôle pour ajouter une signification à ce contrôle. Par exemple, la plupart des contrôles d'édition sont positionnés en regard des étiquettes pour informer l'utilisateur du type d'informations à entrer. Certains contrôles, comme les zones de groupe et les cases d'option, contiennent leurs propres étiquettes. 
  
L'étiquette peut inclure un accélérateur Windows, identifié comme le caractère suivant le signe «&amp;et commercial» (). Appuyer sur la touche d'accès rapide place le focus sur le premier contrôle sans étiquette, sans bouton, après cette étiquette dans la table d'affichage.
  
Les étiquettes multilignes ne sont pas prises en charge. L'affichage de plusieurs lignes requiert plusieurs étiquettes.
  
Il n'est pas possible d'utiliser une étiquette en tant que contrôle d'édition en lecture seule. La différence réside dans le fait qu'un contrôle d'édition peut être sélectionné et copié tandis qu'une étiquette ne peut pas l'être. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

