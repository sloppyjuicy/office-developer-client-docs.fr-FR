---
title: PidTagConflictItems Canonical, propriété
description: Décrit la propriété canonique PidTagConflictItems, qui contient un ou plusieurs ID d’entrée d’éléments impliqués dans une résolution automatique des conflits.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
ms.openlocfilehash: 663296d31cf0457495c22c26655c6ae9df800b8f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817983"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems Canonical, propriété

**S’applique à** : Outlook 2013 | Outlook 2016
  
Contient un ou plusieurs ID d’entrée d’éléments impliqués dans une résolution automatique des conflits.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificateur :  <br/> |0x1098  <br/> |
|Type de propriété :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |ICS  <br/> |

## <a name="remarks"></a>Remarques

Les types d’éléments Microsoft Outlook standard qui prennent en charge la résolution automatique des conflits incluent les types d’éléments standard suivants : éléments de rendez-vous, éléments de contact, éléments de journal, éléments de courrier, éléments de réunion, éléments de note collante et éléments de tâche. Un élément appartenant à une classe de message qui dérive de l’un de ces types d’éléments standard prend également en charge la résolution automatique des conflits. Dans Microsoft Outlook 2003 et Microsoft Office Outlook 2007, lorsque Outlook synchronise des éléments et considère qu’il est possible que la copie résultante ne contienne pas toutes les données essentielles, Outlook stocke les copies en conflit dans le dossier **Conflits**, sous le dossier **Problèmes de synchronisation**.
  
> [!NOTE]
> **Les problèmes de synchronisation** et ses sous-dossiers sont masqués jusqu’à ce que vous cliquez sur **Liste des dossiers** dans le menu **Go** .
  
Un élément expose la propriété **PR_CONFLICT_ITEMS** s’il s’agit de l’un des types d’éléments qui prennent en charge la résolution automatique des conflits, a gagné dans une résolution de conflit ou a été placé dans le dossier **Conflits** en raison d’une résolution de conflit. Le dossier dans lequel l’élément est placé détermine le contenu de **PR_CONFLICT_ITEMS**. Si l’élément se trouve dans un dossier autre que le dossier Conflicts et que l’élément expose la propriété **PR_CONFLICT_ITEMS**, l’élément doit avoir remporté la résolution des **conflits** et **PR_CONFLICT_ITEMS** contiendrait un ou plusieurs ID d’entrée de ces éléments perdus dans la résolution du conflit. Si l’élément se trouve dans le dossier Conflits et que l’élément expose la propriété **PR_CONFLICT_ITEMS**, cet élément doit avoir perdu la résolution des **conflits** et **PR_CONFLICT_ITEMS** contient l’ID d’entrée de l’élément qui a gagné dans la résolution de conflit.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.

[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.

Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.

## <a name="see-also"></a>Voir aussi

[À propos des ajouts MAPI](about-mapi-additions.md)  
[Propriétés MAPI](mapi-properties.md)  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
