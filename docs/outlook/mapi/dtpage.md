---
title: DTPAGE
description: DTPAGE décrit la boîte de dialogue créée à partir d’une table d’affichage par la fonction BuildDisplayTable.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
ms.openlocfilehash: 23383a967c88a73d3503db6251f59d55d9f9dfd9
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815869"
---
# <a name="dtpage"></a>DTPAGE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit la boîte de dialogue générée à partir d’une table d’affichage par la fonction [BuildDisplayTable](builddisplaytable.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a>Members

 **cctl**
  
> Nombre de contrôles pointés par le membre **lpctl** . 
    
 **lpszResourceName**
  
> Pointeur vers le nom ou l’identificateur entier de la ressource de boîte de dialogue. 
    
 **lpszComponent**
  
> Pointeur vers la chaîne qui apparaît dans la section **[Mappages de fichiers d’aide]** dans MAPISVC.INF. Étant donné que **lpszComponent** est dans une union avec le membre **ulItemID** , un seul de ces membres a des données valides. 
    
 **ulItemID**
  
> Identificateur de ressource entier avec une valeur inférieure ou égale à 65535 à partir de laquelle le nom du fichier d’aide peut être lu. Étant donné que **ulItemID** fait partie d’une union avec le membre **lpszComponent** , un seul de ces membres possède des données valides. 
    
 **lpctl**
  
> Pointeur vers un tableau de structures [DTCTL](dtctl.md) , un pour chaque contrôle de la page. 
    
## <a name="remarks"></a>Remarques

Pour identifier le fichier d’aide de la page à onglets, définissez le membre **lpszComponent** sur une chaîne codée en dur ou le membre **ulItemID** sur un identificateur de ressource entier. 
  
Chaque entrée de la section **[Mappages de fichiers d’aide]** dans MAPISVC. INF se compose d’une chaîne de composant, d’au plus 30 caractères, sur le côté gauche et d’un chemin d’accès au fichier d’aide à droite. **UlItemID** et **lpszResourceName** se trouvent dans le paramètre _hInstance_ de **BuildDisplayTable**. Pour plus d’informations, consultez [MAPISVC. Section INF [Mappages de fichiers d’aide](mapisvc-inf-help-file-mappings-section.md)].
  
Bien que **BuildDisplayTable** utilise cette structure pour générer la table d’affichage à partir des ressources de contrôle, la structure **DTPAGE** n’apparaît jamais dans la table d’affichage elle-même. 
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

