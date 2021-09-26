---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 60c84f90c483261fa1feb888f065cbf1b9409a88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630956"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une page à onglets qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
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
  
> Position en mémoire de l’étiquette de chaîne de caractères de l’onglet de page.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabelName.** L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulbLpszComponent**
  
> Position en mémoire d’une chaîne de caractères identifiant la section **[Mappages des fichiers d’aide]** dans MAPISVC. Fichier de configuration INF ou 0. Nom de fichier apparaissant dans MAPISVC. La section INF peut être utilisée par un utilisateur pour accéder  à l’aide étendue de la page à onglets en cliquant sur le bouton Aide de la boîte de dialogue. Pour plus d’informations sur les entrées dans MAPISVC. INF, voir [Format de fichier de MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Identificateur unique de la page à onglets dans la chaîne définie par le membre **ulbLpszComponent.** Le **membre ulbLpszComponent** et le membre **ulContext** doivent  tous deux être non zéro pour que le bouton Aide fonctionne. Si cet identificateur est zéro et que la chaîne du composant est NULL, aucune aide n’est associée à la page. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLPAGE** décrit une page à onglets d’un contrôle utilisé pour séparer plusieurs boîtes de dialogue associées. En règle générale, ces boîtes de dialogue sont des feuilles de propriétés pour l’affichage des options de configuration, de message ou de destinataire. En cliquant sur l’onglet, l’utilisateur peut passer d’une feuille à une autre. 
  
La chaîne de composant et l’identificateur de contexte fournissent des informations pour savoir si l’aide étendue est disponible pour la page à onglets. Si une aide étendue est disponible, la chaîne de composant et l’identificateur de contexte fournissent des informations sur la façon d’y accéder. La chaîne de composant est m m filée vers le fichier d’aide . l’identificateur de contexte est map pour la rubrique d’aide initiale. Si l’identificateur de contexte est zéro et que la chaîne du composant est NULL, l’aide étendue n’est pas disponible.
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

