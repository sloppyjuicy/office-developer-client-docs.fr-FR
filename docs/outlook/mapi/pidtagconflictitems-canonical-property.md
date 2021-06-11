---
title: Propriété canonique PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338016"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propriété canonique PidTagConflictItems

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un ou plusieurs ID d’entrée d’éléments impliqués dans une résolution automatique de conflit.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificateur :  <br/> |0x1098  <br/> |
|Type de propriété :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Remarques

Les types d’éléments Microsoft Outlook standard qui la prise en charge de la résolution automatique des conflits incluent les types d’éléments standard suivants : éléments de rendez-vous, éléments de contact, éléments de journal, éléments de courrier, éléments de réunion, éléments de note pense-tout et éléments de tâche. Un élément appartenant à une classe de message qui dérive de l’un de ces types d’éléments standard prend également en charge la résolution automatique des conflits. Dans Microsoft Outlook 2003 et Microsoft Office Outlook 2007, lorsque Outlook synchronise les éléments et considère qu’il est possible que la copie résultante ne contienne pas toutes les données essentielles, Outlook stocke les **copies** en conflit dans le dossier Conflits, sous le dossier Problèmes de synchronisation.  
  
> [!NOTE]
> **Les problèmes de synchronisation et** ses sous-dossiers sont masqués jusqu’à ce que vous cliquiez sur **Liste** des dossiers dans le menu **Go.** 
  
Un élément expose la propriété PR_CONFLICT_ITEMS s’il s’agit de l’un des types d’éléments qui  supportent la résolution automatique des conflits, s’il a été gagné dans une résolution de conflit ou **s’il a** été placé dans le dossier Conflits en raison d’une résolution de conflit. Le dossier dans lequel l’élément est placé détermine le contenu de **PR_CONFLICT_ITEMS**. Si l’élément se trouve dans un dossier autre que le dossier **Conflits** et que l’élément expose la propriété **PR_CONFLICT_ITEMS,** l’élément doit avoir obtenu la résolution de conflit et **PR_CONFLICT_ITEMS** contient un ou plusieurs ID d’entrée des éléments perdus dans la résolution de conflit. Si l’élément se trouve dans le dossier **Conflits** et que l’élément expose la propriété **PR_CONFLICT_ITEMS,** cet élément doit avoir perdu la résolution de conflit et **PR_CONFLICT_ITEMS** contient l’ID d’entrée de l’élément qui a gagné dans la résolution de conflit. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

