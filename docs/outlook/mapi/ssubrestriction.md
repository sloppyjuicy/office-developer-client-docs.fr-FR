---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581957"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une restriction objet secondaire qui permet de filtrer les lignes de pièce jointe ou un tableau de destinataire d’un message.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Members

 **ulSubObject**
  
> Type d’objet secondaire en guise de la cible de la restriction. Les valeurs possibles sont les suivantes : 
    
PR_MESSAGE_RECIPIENTS 
  
> Appliquer la restriction à la table des destinataires d’un message. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Appliquer la restriction à la table des pièces jointes d’un message. 
    
 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) . 
    
## <a name="remarks"></a>Remarques

Restrictions de l’objet sous-fonctionnalités ne sont pas pris en charge par toutes les tables. En règle générale, uniquement le dossier contenu tables et dossiers de résultats de recherche les prendre en charge. Par exemple, restrictions de l’objet sous-sites sont utilisées pour rechercher un message qui a un type particulier de pièce jointe ou un destinataire. 
  
Si une implémentation ne gère pas les restrictions de l’objet secondaire, elle renvoie MAPI_E_TOO_COMPLEX à partir de ses méthodes [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) . 
  
Pour une présentation générale du fonctionnement des restrictions, voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

