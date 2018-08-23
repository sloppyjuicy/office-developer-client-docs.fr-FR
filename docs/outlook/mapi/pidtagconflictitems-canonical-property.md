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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3ff428d96de40e70e63659c5a3e5fa1c7cf0d564
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569112"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propriété canonique PidTagConflictItems

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un ou plusieurs identificateurs d’éléments qui ont été impliquées dans une résolution de conflit automatique d’entrée.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificateur :  <br/> |0x1098  <br/> |
|Type de propriété :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |PARTAGE DE CONNEXION INTERNET  <br/> |
   
## <a name="remarks"></a>Remarques

Les types d’éléments Microsoft Outlook standards qui prennent en charge la résolution automatique de conflit sont les types d’éléments standard suivantes : éléments de rendez-vous, contacts, éléments de journal, éléments de courrier, éléments de réunion, éléments pense-bête et éléments de tâche. Un élément appartenant à une classe de message dérivée d’une de ces types d’éléments standard également prend en charge la résolution automatique de conflit. Dans Microsoft Outlook 2003 et Microsoft Office Outlook 2007, lorsque Outlook synchronise les éléments et considère qu’il est possible que la copie résultante ne peut pas contenir toutes les données essentielles, Outlook stocke les copies en conflit dans les **conflits** dossier sous le dossier **Problèmes de synchronisation** . 
  
> [!NOTE]
> **Problèmes de synchronisation** et ses sous-dossiers sont masqués jusqu'à ce que vous cliquez sur **Liste des dossiers** dans le menu **Atteindre** . 
  
Un élément expose la propriété **PR_CONFLICT_ITEMS** si elle est un des types d’éléments qui prennent en charge la résolution automatique de conflit, a été dans une résolution de conflit ou a été placé dans le dossier **conflits** en raison d’une résolution de conflit. Le dossier dans lequel se trouve l’élément détermine le contenu de **PR_CONFLICT_ITEMS**. Si l’élément se trouve dans un dossier autre que le dossier **conflits** et l’élément expose la propriété **PR_CONFLICT_ITEMS** , l’élément doit avoir conclues la résolution de conflit et **PR_CONFLICT_ITEMS** contient un ou plusieurs identificateurs d’entrée de ces éléments perdus au cours de la résolution de conflit. Si l’élément se trouve dans le dossier **conflits** et l’élément expose la propriété **PR_CONFLICT_ITEMS** , cet élément doit avoir perdu la résolution de conflit et **PR_CONFLICT_ITEMS** contient l’identificateur d’entrée de l’élément conclues dans le conflit résolution. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

