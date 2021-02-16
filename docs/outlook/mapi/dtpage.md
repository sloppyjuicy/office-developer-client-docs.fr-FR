---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408221"
---
# <a name="dtpage"></a>DTPAGE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit la boîte de dialogue qui est conçue à partir d’un tableau d’affichage par la [fonction BuildDisplayTable.](builddisplaytable.md) 
  
|||
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
  
> Nombre de contrôles pointés par **le membre lpctl.** 
    
 **lpszResourceName**
  
> Pointeur vers le nom ou l’identificateur de la boîte de dialogue. 
    
 **lpszComponent**
  
> Pointeur vers la chaîne qui apparaît dans la section [Mappages des fichiers **d’aide]** dans MAPISVC.INF. Étant **donné que lpszComponent** est en union avec le membre **ulItemID,** un seul de ces membres possède des données valides. 
    
 **ulItemID**
  
> Identificateur de ressource d’un nombre complet avec une valeur inférieure ou égale à 65535 à partir de laquelle le nom du fichier d’aide peut être lu. Étant **donné qu’ulItemID** est en union avec le membre **lpszComponent,** un seul de ces membres possède des données valides. 
    
 **lpctl**
  
> Pointeur vers un tableau de structures [DTCTL,](dtctl.md) un pour chaque contrôle de la page. 
    
## <a name="remarks"></a>Remarques

Pour identifier le fichier d’aide de la page à onglets, définissez le membre **lpszComponent** sur une chaîne codée en dur ou le membre **ulItemID** sur un identificateur de ressource entière. 
  
Chaque entrée de la section **[Mappages des fichiers d’aide]** dans MAPISVC. INF se compose d’une chaîne de composants, de 30 caractères au plus, à gauche et d’un chemin d’accès au fichier d’aide à droite. **UlItemID et** **lpszResourceName** se trouvent dans le paramètre _hInstance_ de **BuildDisplayTable**. Pour plus d’informations, [voir MAPISVC. Section INF [Mappages des fichiers d’aide]](mapisvc-inf-help-file-mappings-section.md).
  
Bien **que BuildDisplayTable** utilise cette structure pour créer la table d’affichage à partir des ressources de contrôle, la structure **DTPAGE** n’apparaît jamais dans le tableau d’affichage lui-même. 
  
Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

