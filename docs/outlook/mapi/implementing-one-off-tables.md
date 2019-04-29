---
title: Implémentation de tables ponctuelles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421640"
---
# <a name="implementing-one-off-tables"></a>Implémentation de tables ponctuelles

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Votre fournisseur peut implémenter une ou plusieurs tables ponctuelles. Une table ponctuelle est une liste récapitulative des modèles uniques utilisés pour créer des destinataires, directement dans un conteneur ou dans la liste des destinataires d'un message sortant. Un modèle isolé est un formulaire que les utilisateurs emploient pour entrer des données relatives à un type d'adresse particulier. Lorsque l'utilisateur a terminé d'utiliser le modèle, le fournisseur crée le nouveau destinataire et l'ajoute au message. En règle générale, chaque modèle gère un seul type d'adresse. Toutefois, il est possible qu'un modèle gère plusieurs types ou que plusieurs modèles gèrent le même type. 
  
Votre fournisseur doit prendre en charge la méthode **OpenEntry** pour chaque modèle qu'il inclut dans la table ponctuelle. L'implémentation de **OpenEntry** doit récupérer une table d'affichage pour le modèle. MAPI utilise la table d'affichage pour faire en sorte que le modèle soit visible par l'utilisateur. 
  
Bien que la plupart des lignes des tables ponctuelles représentent des modèles, certaines lignes peuvent être utilisées pour catégoriser ou regrouper des modèles. Si une ligne d'une table ponctuelle représente un modèle est indiquée par la valeur de sa colonne **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). Les lignes qui représentent des modèles ont la colonne PR_SELECTABLE définie sur TRUE; les lignes qui ne représentent pas de modèles ont la valeur FALSe.
  
MAPI définit trois types de tables ponctuelles:
  
- Table ponctuelle reflétant les modèles pris en charge par un conteneur individuel
    
- Table ponctuelle reflétant tous les modèles pris en charge par votre fournisseur 
    
- Une table ponctuelle reflétant tous les modèles pris en charge par tous les fournisseurs du profil, ainsi que ceux pris en charge par MAPI
    
Les deux premiers types sont implémentés par les fournisseurs qui prennent en charge les destinataires de la création, soit sur un message, soit dans un conteneur. Votre fournisseur peut inclure le même ensemble ou un ensemble de modèles différent dans ses tables ponctuelles. La principale différence entre ces deux types est que votre table de fournisseurs doit inclure des modèles pour la création de destinataires qui peuvent être utilisés sur les messages sortants et que votre table de conteneurs doit inclure des modèles pour la création de destinataires à ajouter à votre conteneur. Un conteneur ne peut prendre en charge qu'un ensemble restreint de modèles, mais la table ponctuelle du fournisseur doit inclure tous les modèles pris en charge par le fournisseur.
  
Le troisième type de table ponctuelle est implémenté par MAPI; les fournisseurs y accèdent en appelant [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). La table ponctuelle MAPI est l'Union de toutes les tables des fournisseurs; Elle inclut tous les modèles pris en charge par tous les fournisseurs dans le profil. Il inclut également des modèles pris en charge par MAPI. Votre fournisseur peut utiliser ce tableau à la place de la table demandée pour un conteneur. Toutefois, les modèles de ce tableau peuvent également être utilisés pour créer des destinataires pour les messages sortants.
  

