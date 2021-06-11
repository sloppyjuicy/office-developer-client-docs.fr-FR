---
title: Tables MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 840c34a64cd0478be8f208799653b9916f50079d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437083"
---
# <a name="mapi-tables"></a>Tables MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table MAPI est un objet MAPI utilisé pour afficher une collection de propriétés appartenant à d’autres objets MAPI d’un type particulier. Les tableaux MAPI sont structurés au format ligne et colonne avec chaque ligne représentant un objet et chaque colonne représentant une propriété de l’objet. L’une des propriétés généralement incluses dans chaque ligne est la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), un identificateur qui peut être utilisé pour ouvrir et modifier l’objet. 
  
Étant donné que les lignes contiennent des valeurs de propriété, la récupération d’une ligne à partir d’un tableau est similaire à l’obtention d’un ensemble de propriétés directement à partir de l’objet représenté par la ligne. Les deux opérations entraînent la récupération d’un tableau de valeurs de propriétés. La principale différence est la gestion des propriétés binaires et de chaîne longue. Pour l’inclusion dans un tableau, certains implémenteurs de table tronqué ces propriétés à 255 octets. Lorsqu’elle est récupérée directement à partir de l’objet, la valeur complète est toujours disponible.
  
Les tableaux sont implémentés par les fournisseurs de carnets d’adresses et de magasins de messages et par MAPI, en fonction du type de table et des objets qu’elle int.. Un fournisseur de magasins de messages implémente des dossiers et une table des matières pour chaque dossier qui inclut des informations sur les messages du dossier. Un fournisseur de carnet d’adresses implémente des conteneurs de carnet d’adresses et une table hiérarchique qui indique leur organisation. MAPI implémente plusieurs tables différentes, certaines pour une utilisation par les applications clientes, d’autres pour l’utilisation par les fournisseurs de services et d’autres pour une utilisation par les deux. La table d’état est unique dans le fait que MAPI fournit finalement le tableau, mais les lignes sont composées de contributions de tous les types de fournisseurs de services en plus de MAPI. 
  
L’illustration suivante montre l’une des utilisations fréquentes d’une table dans MAPI : pour afficher le contenu d’un dossier. À droite se trouve l’affichage de deux messages, comme cela peut apparaître dans une application cliente de messagerie classique. L’affichage contient quatre éléments d’informations sur chaque message : l’expéditeur, le destinataire, l’objet et le texte du message. Chaque information correspond à une propriété du message.
  
À gauche se trouve une vue de la table des matières qui inclut ces deux messages. Alors que la table des matières peut contenir dix lignes, car le dossier contient dix messages, chaque ligne contenant plus de trois colonnes, cet affichage particulier est limité à deux lignes et trois colonnes seulement.
  
Le tableau suivant indique les propriétés qui font la colonne définie pour l’affichage tableau.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nom de l’expéditeur  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Date et heure d’envoi du message  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Ligne d’objet du message  <br/> |
   
Notez que l’ensemble des propriétés affichées dans le message ne sont pas identiques à l’ensemble des colonnes affichées dans le tableau. L’implémenteur de la table, dans ce cas un fournisseur de magasin de messages, fournit un ensemble par défaut de colonnes dans un ordre par défaut. Le client peut modifier cet ensemble de colonnes en demandant des colonnes supplémentaires ou en rejetant les colonnes par défaut, et demander qu’ils soient commandés d’une manière spécifique. Le client peut également trier les lignes en fonction de la valeur d’une ou de plusieurs colonnes.
  
**Utilisation d’un tableau pour afficher le contenu du dossier**
  
![Utilisation d’un tableau pour afficher le contenu d’un dossier]À l’aide(media/amapi_54.gif "d’un tableau pour afficher le contenu du dossier")
  
Il existe deux interfaces pour l’utilisation des tableaux :
  
- [IMAPITable : IUnknown](imapitableiunknown.md) offre aux clients et aux fournisseurs de services une vue en lecture seule des données sous-jacentes du tableau, ce qui leur permet d’afficher et de modifier uniquement la présentation. Plusieurs utilisateurs peuvent accéder simultanément aux mêmes données avec **IMAPITable**. **IMAPITable** est implémenté par MAPI et par des fournisseurs de services. 
    
- [ITableData : IUnknown](itabledataiunknown.md) donne aux clients et aux fournisseurs de services un accès en lecture/écriture aux données sous-jacentes de la table, ce qui leur permet d’apporter des modifications permanentes. **IMAPITable** est implémenté par MAPI et utilisé principalement par les fournisseurs de services qui y accèdent en appelant [la fonction CreateTable.](createtable.md) **L’implémentation ITableData** contient toutes les données de la table et toutes les restrictions associées en mémoire, ce qui la rend inadaptée pour une utilisation avec de très grandes tables. Les restrictions composées et les opérations complexes telles que la catégorisation ne sont pas pris en mesure. 
    
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI](mapi-concepts.md)

