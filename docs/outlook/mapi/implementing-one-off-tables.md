---
title: Mise en œuvre One-Off tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
ms.openlocfilehash: 68a7f7eb7d74fb97cb9042f1b531327e9cb5229b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369664"
---
# <a name="implementing-one-off-tables"></a>Mise en œuvre One-Off tables

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre fournisseur peut implémenter une ou plusieurs tables one-off. Un tableau unique est une liste récapitulatif des modèles unique utilisés pour créer des destinataires, soit directement dans un conteneur, soit dans la liste des destinataires d’un message sortant. Un modèle unique est un formulaire que les utilisateurs utilisent pour entrer des données relatives à un type particulier d’adresse. Lorsque l’utilisateur a terminé de travailler avec le modèle, votre fournisseur crée le nouveau destinataire et l’ajoute au message. En règle générale, chaque modèle gère un type d’adresse unique. Toutefois, il est possible pour un modèle de gérer plusieurs types ou pour plusieurs modèles de gérer le même type. 
  
Votre fournisseur doit prendre en charge **la méthode OpenEntry** pour chaque modèle qu’il inclut dans la table unique. L’implémentation **d’OpenEntry** doit récupérer une table d’affichage pour le modèle. MAPI utilise le tableau d’affichage pour rendre le modèle visible par l’utilisateur. 
  
Bien que la plupart des lignes dans des tableaux non personnalisés représentent des modèles, certaines de ces lignes peuvent être utilisées pour catégoriser ou grouper des modèles. La valeur de sa colonne ([PidTagSelectable](pidtagselectable-canonical-property.md)) indique si une ligne d’un **PR_SELECTABLE** tableau unique représente un modèle ou non. Les lignes qui représentent des modèles ont la PR_SELECTABLE colonne définie sur TRUE ; pour les lignes qui ne représentent pas les modèles, la mise en page est définie sur FALSE.
  
MAPI définit trois types de tables one-off :
  
- Tableau unique qui reflète les modèles qu’un conteneur individuel prend en charge
    
- Tableau unique qui reflète tous les modèles que votre fournisseur prend en charge 
    
- Tableau unique qui reflète tous les modèles que tous les fournisseurs du profil prend en charge, ainsi que certains modèles que MAPI prend en charge
    
Les deux premiers types sont implémentés par des fournisseurs qui prendre en charge les destinataires de création, soit dans un message, soit dans un conteneur. Votre fournisseur peut inclure le même ensemble ou un autre ensemble de modèles dans ses tables unique. La principale différence entre les deux types est que votre table de fournisseurs doit inclure des modèles de création de destinataires qui peuvent être utilisés sur les messages sortants et que votre table de conteneur doit inclure des modèles pour la création de destinataires à ajouter à votre conteneur. Un conteneur peut uniquement prendre en charge un ensemble restreint de modèles, mais le tableau unique fournisseur doit inclure chaque modèle que le fournisseur prend en charge.
  
Le troisième type de table one-off est implémenté par MAPI ; les fournisseurs y accèdent en appelant [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). La table MAPI est l’union de toutes les tables de fournisseurs ; il inclut tous les modèles pris en charge par chaque fournisseur dans le profil. Il inclut également les modèles pris en charge par MAPI. Votre fournisseur peut utiliser cette table à la place de la table demandée pour un conteneur. Toutefois, les modèles de ce tableau peuvent également être utilisés pour créer des destinataires pour les messages sortants.
  

