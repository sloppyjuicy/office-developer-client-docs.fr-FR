---
title: DTBLPAGE
description: DTBLPAGE décrit une page à onglets qui sera utilisée dans une boîte de dialogue générée à partir d’une table d’affichage.
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
ms.openlocfilehash: aa1929f6b518899ac02c613e8b5a935817515e97
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815673"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une page à onglets qui sera utilisée dans une boîte de dialogue créée à partir d’une table d’affichage. 
  
|Propriété |Valeur |
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
  
> Masque de bits des indicateurs utilisés pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabelName** . L’indicateur suivant peut être défini : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, l’étiquette est au format ANSI.
    
 **ulbLpszComponent**
  
> Position en mémoire d’une chaîne de caractères identifiant la section **[Mappages de fichiers d’aide]** dans MAPISVC. Fichier de configuration INF ou 0. Nom de fichier qui s’affiche dans MAPISVC. La section INF peut être utilisée par un utilisateur pour accéder à l’aide étendue pour la page à onglets en cliquant sur le bouton **Aide** dans la boîte de dialogue. Pour plus d’informations sur les entrées dans MAPISVC. INF, voir [Format de fichier de MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Identificateur unique de la page à onglets dans la chaîne définie par le membre **ulbLpszComponent** . Le membre **ulbLpszComponent** et le membre **ulContext** doivent tous deux être différent de zéro pour que le bouton **d’aide** fonctionne. Si cet identificateur est égal à zéro et que la chaîne de composant est NULL, aucune aide n’est associée à la page. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLPAGE** décrit une page à onglets, un contrôle utilisé pour séparer plusieurs boîtes de dialogue associées. En règle générale, ces boîtes de dialogue sont des feuilles de propriétés permettant d’afficher les options de configuration, de message ou de destinataire. En cliquant sur l’onglet, l’utilisateur peut passer d’une feuille à une autre. 
  
La chaîne de composant et l’identificateur de contexte fournissent des informations sur la disponibilité de l’aide étendue pour la page à onglets. Si l’aide étendue est disponible, la chaîne de composant et l’identificateur de contexte fournissent des informations sur la façon d’y accéder. La chaîne de composant est mappée au fichier d’aide ; l’identificateur de contexte correspond à la rubrique d’aide initiale. Si l’identificateur de contexte est égal à zéro et que la chaîne de composant est NULL, l’aide étendue n’est pas disponible.
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

