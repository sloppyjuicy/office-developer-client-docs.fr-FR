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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338016"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propriété canonique PidTagConflictItems

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un ou plusieurs identificateurs d'entrée d'éléments impliqués dans une résolution automatique des conflits.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificateur :  <br/> |0x1098  <br/> |
|Type de propriété:  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |DÛMENT  <br/> |
   
## <a name="remarks"></a>Remarques

Les types d'éléments Microsoft Outlook standard qui prennent en charge la résolution automatique des conflits incluent les types d'éléments standard suivants: les éléments de rendez-vous, les éléments de contact, les éléments de journal, les éléments de courrier, les éléments de réunion, les éléments de notes de pense-bête et les tâches. Un élément appartenant à une classe de message qui dérive de l'un de ces types d'éléments standard prend également en charge la résolution automatique des conflits. Dans Microsoft Outlook 2003 et Microsoft Office Outlook 2007, lorsque Outlook synchronise les éléments et estime qu'il est possible que la copie résultante ne contienne pas toutes les données essentielles, Outlook stocke les copies conflictuelles dans les **conflits** . dossier, sous le dossier **problèmes de synchronisation** . 
  
> [!NOTE]
> Les **problèmes de synchronisation** et ses sous-dossiers sont masqués jusqu'à ce que vous cliquiez sur liste des **dossiers** dans le menu **atteindre** . 
  
Un élément expose la propriété **PR_CONFLICT_ITEMS** s'il s'agit d'un des types d'éléments qui prennent en charge la résolution automatique des conflits, qu'il a remporté une résolution de conflit ou qu'il a été placé dans le dossier **conflits** en raison d'une résolution de conflit. Le dossier dans lequel l'élément est placé détermine le contenu de **PR_CONFLICT_ITEMS**. Si l'élément se trouve dans un dossier autre que le dossier **conflits** et que l'élément expose la propriété **PR_CONFLICT_ITEMS** , l'élément doit avoir gagné la résolution de conflit et **PR_CONFLICT_ITEMS** contenir un ou plusieurs identificateurs d'entrée de les éléments perdus dans la résolution des conflits. Si l'élément se trouve dans le dossier **conflits** et que l'élément expose la propriété **PR_CONFLICT_ITEMS** , cet élément doit avoir perdu la résolution de conflit, et **PR_CONFLICT_ITEMS** contient l'ID d'entrée de l'élément qui a été remporté dans le conflit. résolution. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données d'objet de messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

