---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: Décrit une restriction de sous-objet utilisée pour filtrer les lignes de la table des destinataires ou des pièces jointes d’un message.
ms.openlocfilehash: f869c4441bd49e4a511f42bef50d22b775871aed
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455922"
---
# <a name="ssubrestriction"></a>SSubRestriction

**S’applique à** : Outlook 2013 | Outlook 2016
  
Décrit une restriction de sous-objet utilisée pour filtrer les lignes de la table des destinataires ou des pièces jointes d’un message.
  
|Propriété |Valeur |
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
  
> Type de sous-objet à cibler pour la restriction. Les valeurs possibles sont les suivantes :

PR_MESSAGE_RECIPIENTS
  
> Appliquez la restriction à la table des destinataires d’un message.

PR_MESSAGE_ATTACHMENTS
  
> Appliquez la restriction à la table des pièces jointes d’un message.

 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) .

## <a name="remarks"></a>Remarques

Les restrictions de sous-objet ne sont pas pris en charge par toutes les tables. En règle générale, seuls les tableaux de contenu de dossier et les dossiers de résultats de recherche les prend en charge. Par exemple, les restrictions de sous-objet sont utilisées pour rechercher un message qui a un type particulier de pièce jointe ou de destinataire.
  
Si une implémentation ne prend pas en charge les restrictions de sous-objet, elle renvoie MAPI_E_TOO_COMPLEX à partir de ses méthodes [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) .
  
Pour une discussion générale sur le fonctionnement des restrictions, voir [À propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

[SRestriction](srestriction.md)
 [Structures MAPI](mapi-structures.md)
