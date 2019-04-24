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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287104"
---
# <a name="dtpage"></a>DTPAGE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit la boîte de dialogue qui est générée à partir d'une table d'affichage par la fonction [BuildDisplayTable](builddisplaytable.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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

 **CCTL**
  
> Nombre de contrôles vers lesquels pointe le membre **lpctl** . 
    
 **lpszResourceName**
  
> Pointeur vers le nom ou l'identificateur entier de la ressource de la boîte de dialogue. 
    
 **lpszComponent**
  
> Pointeur vers la chaîne qui apparaît dans la section **[Help file Mappings] du fichier** MAPISVC. inf. Étant donné que **lpszComponent** est dans une Union avec le membre **ulItemID** , un seul de ces membres a des données valides. 
    
 **ulItemID**
  
> Identificateur de ressource entier avec une valeur inférieure ou égale à 65535 à partir de laquelle le nom du fichier d'aide peut être lu. Étant donné que **ulItemID** est dans une Union avec le membre **lpszComponent** , un seul de ces membres a des données valides. 
    
 **lpctl**
  
> Pointeur vers un tableau de structures [DTCTL](dtctl.md) , un pour chaque contrôle sur la page. 
    
## <a name="remarks"></a>Remarques

Pour identifier le fichier d'aide de la page à onglets, définissez le membre **lpszComponent** sur une chaîne codée en dur ou le membre **ulItemID** sur un identificateur de ressource Integer. 
  
Chaque entrée de la section **[Help file Mappings]** dans MAPISVC. INF se compose d'une chaîne de composant, pas de plus de 30 caractères, du côté gauche et d'un chemin d'accès au fichier d'aide à droite. **UlItemID** et **lpszResourceName** sont trouvés dans le paramètre _HINSTANCE_ de **BuildDisplayTable**. Pour plus d'informations, consultez la rubrique [MAPISVC. Section INF [mappages de fichiers d'aide]](mapisvc-inf-help-file-mappings-section.md).
  
Bien que **BuildDisplayTable** utilise cette structure pour créer la table d'affichage à partir des ressources de contrôle, la structure **DTPAGE** n'apparaît jamais dans le tableau proprement dit. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

