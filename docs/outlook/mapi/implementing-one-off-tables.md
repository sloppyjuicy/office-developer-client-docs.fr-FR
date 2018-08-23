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
ms.openlocfilehash: b86ec02c0255d892c42a9be9610d31b76041822c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579108"
---
# <a name="implementing-one-off-tables"></a>Implémentation de tables ponctuelles

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Votre fournisseur peut implémenter une ou plusieurs tables unique. Une table unique est une liste récapitulative de modèles uniques utilisés pour créer des destinataires, soit directement dans un conteneur, ou dans la liste des destinataires d’un message sortant. Un modèle unique est un utilisent les utilisateurs de formulaire pour la saisie de données par rapport à un type particulier d’adresse. Lorsque l’utilisateur est terminé fonctionne avec le modèle, votre fournisseur crée le nouveau destinataire et l’ajoute au message. En règle générale, chaque modèle gère un type d’adresse unique. Toutefois, il est possible d’un modèle de gérer plusieurs types ou pour gérer le même type de plusieurs modèles. 
  
Votre fournisseur doit prendre en charge la méthode **OpenEntry** de chaque modèle contient dans le tableau unique. L’implémentation de **OpenEntry** doit récupérer un tableau d’affichage pour le modèle. MAPI utilise la table d’affichage pour rendre le modèle visible à l’utilisateur. 
  
La plupart des lignes de tableaux uniques représentent des modèles, certaines des lignes peuvent être utilisé pour classer, ou un groupe, les modèles. Représente une ligne dans une table unique ou non un modèle est indiqué par la valeur de la colonne **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). Les lignes qui représentent les modèles ont la colonne PR_SELECTABLE définie sur TRUE ; les lignes qui ne représentent pas les modèles ont la valeur False.
  
MAPI définit trois types de tables uniques :
  
- Une table unique qui reflète les modèles prenant en charge un conteneur
    
- Une table unique qui reflète tous les modèles qui prend en charge par votre fournisseur 
    
- Une table unique qui reflète tous les modèles que tous les fournisseurs dans le profil prennent en charge plus certains qui prend en charge de MAPI
    
Les deux premiers types sont implémentés par les fournisseurs qui prennent en charge les destinataires de la création, sur un message ou dans un conteneur. Votre fournisseur peut inclure le même ensemble ou un ensemble de modèles différent dans ses tables uniques. La principale différence entre les deux types est que votre table de fournisseur doit inclure des modèles pour la création de destinataires qui peuvent être utilisés sur les messages sortants et votre table de conteneur doit inclure des modèles pour la création de destinataires à ajouter à votre conteneur. Un conteneur peut prendre uniquement en charge un ensemble limité de modèles, mais le tableau uniques fournisseur doit inclure chaque modèle le fournisseur prend en charge.
  
Le type de table unique tiers est implémenté par MAPI ; fournisseurs d’y accéder en appelant [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Le tableau unique MAPI est l’union de toutes les tables fournisseur ; Il inclut tous les modèles pris en charge par chaque fournisseur dans le profil. Il inclut également des modèles pris en charge par MAPI. Votre fournisseur peut utiliser ce tableau à la place de la table demandée pour un conteneur. Toutefois, les modèles de cette table peuvent également servir pour la création de destinataires pour les messages sortants.
  

