---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340116"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une page à onglets qui sera utilisée dans une boîte de dialogue construite à partir d'une table d'affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de l'étiquette de la chaîne de caractères pour l'onglet page.
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format de l'étiquette désignée par le membre **ulbLpszLabelName** . L'indicateur suivant peut être défini: 
    
MAPI_UNICODE 
  
> L'étiquette est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.
    
 **ulbLpszComponent**
  
> Position en mémoire d'une chaîne de caractères identifiant la section **[Help file Mappings] du fichier** MAPISVC. Fichier de configuration INF ou 0. Nom de fichier apparaissant dans le fichier MAPISVC. INF peut être utilisée par un utilisateur pour accéder à une aide étendue pour la page à onglets en cliquant sur le bouton **aide** dans la boîte de dialogue. Pour plus d'informations sur les entrées dans MAPISVC. INF, consultez le [format de fichier MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Identificateur unique de la page à onglets dans la chaîne définie par le membre **ulbLpszComponent** . Le membre **ulbLpszComponent** et le membre **ulContext** doivent avoir une valeur différente de zéro pour que le bouton **aide** fonctionne. Si cet identificateur est égal à zéro et que la chaîne du composant est NULL, aucune aide n'est associée à la page. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLPAGE** décrit une page à onglets qui est un contrôle utilisé pour séparer plusieurs boîtes de dialogue associées. En règle générale, ces boîtes de dialogue sont des feuilles de propriétés permettant d'afficher les options de configuration, de message ou de destinataire. En cliquant sur l'onglet, l'utilisateur peut passer d'une feuille à une autre. 
  
La chaîne de composant et l'identificateur de contexte fournissent des informations indiquant si l'aide étendue est disponible pour la page à onglets. Si l'aide étendue est disponible, la chaîne de composant et l'identificateur de contexte fournissent des informations sur la façon d'y accéder. La chaîne de composant est mappée sur le fichier d'aide; l'identificateur de contexte correspond à la rubrique d'aide initiale. Si l'identificateur de contexte est zéro et que la chaîne de composant est NULL, l'aide étendue n'est pas disponible.
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

