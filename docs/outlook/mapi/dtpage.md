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
ms.openlocfilehash: a187245b2594282bc9908b3075852440f418af2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783252"
---
# <a name="dtpage"></a>DTPAGE

  
  
**S’applique à**: Outlook 
  
Décrit la boîte de dialogue qui est générée à partir d’une table d’affichage par la fonction [BuildDisplayTable](builddisplaytable.md) . 
  
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

## <a name="members"></a>Membres

 **cctl**
  
> Nombre de contrôles vers laquelle pointe le membre **lpctl** . 
    
 **lpszResourceName**
  
> Pointeur vers l’identificateur de nom ou entier de la ressource de boîte de dialogue. 
    
 **lpszComponent**
  
> Pointeur vers la chaîne qui s’affiche dans la section **[Help File Mappings]** dans MAPISVC.INF. **LpszComponent** étant une union avec le membre **ulItemID** , une seule de ces membres comporte des données valides. 
    
 **ulItemID**
  
> Identificateur de ressources entier avec une valeur inférieure ou égale à 65535 à partir de laquelle le nom de fichier peut être lue. **UlItemID** étant une union avec le membre **lpszComponent** , une seule de ces membres comporte des données valides. 
    
 **lpctl**
  
> Pointeur vers un tableau de structures [DTCTL](dtctl.md) , un pour chaque contrôle sur la page. 
    
## <a name="remarks"></a>Remarques

Pour identifier le fichier d’aide pour la page à onglets, affectez le membre **lpszComponent** en chaîne codée en dur ou le membre **ulItemID** un identificateur de ressource entier. 
  
Chaque entrée dans la section **[Help File Mappings]** dans le fichier MAPISVC.inf. INF se compose d’une chaîne de composant, pas plue de 30 caractères, sur le côté gauche et un chemin de fichier d’aide sur la droite. À la fois **ulItemID** et **lpszResourceName** sont trouvent dans le paramètre _hInstance_ de **BuildDisplayTable**. Pour plus d’informations, voir [fichier MAPISVC.inf. INF [aide File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).
  
Bien que **BuildDisplayTable** utilise cette structure pour créer le tableau d’affichage de ressources du contrôle, la structure **DTPAGE** n’apparaît jamais dans la table d’affichage lui-même. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

