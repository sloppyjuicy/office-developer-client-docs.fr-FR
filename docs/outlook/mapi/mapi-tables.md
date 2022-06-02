---
title: Tables MAPI
description: Une table MAPI est un objet MAPI utilisé pour afficher une collection de propriétés appartenant à d’autres objets MAPI d’un type particulier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
ms.openlocfilehash: 7aba0594c242629489365551ce7dc334b83b8d8f
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827988"
---
# <a name="mapi-tables"></a>Tables MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table MAPI est un objet MAPI utilisé pour afficher une collection de propriétés appartenant à d’autres objets MAPI d’un type particulier. Les tables MAPI sont structurées dans un format de ligne et de colonne avec chaque ligne représentant un objet et chaque colonne représentant une propriété de l’objet. L’une des propriétés généralement incluses dans chaque ligne est la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), un identificateur qui peut être utilisé pour ouvrir et modifier l’objet. 
  
Étant donné que les lignes contiennent des valeurs de propriété, la récupération d’une ligne à partir d’une table est similaire à l’obtention d’un ensemble de propriétés directement à partir de l’objet représenté par la ligne. Les deux opérations entraînent la récupération d’un tableau de valeurs de propriété. La principale différence réside dans la gestion des propriétés binaires et de chaîne longue. Pour l’inclusion dans une table, certains implémenteurs de table tronquent ces propriétés à 255 octets. Lorsqu’elle est récupérée directement à partir de l’objet, la valeur complète est toujours disponible.
  
Les tables sont implémentées par les fournisseurs de carnets d’adresses et de magasins de messages et par MAPI, en fonction du type de table et des objets qu’il contient. Un fournisseur de magasin de messages implémente des dossiers et une table de contenu pour chaque dossier qui inclut des informations sur les messages dans le dossier. Un fournisseur de carnets d’adresses implémente des conteneurs de carnets d’adresses et une table de hiérarchie qui montre leur organisation. MAPI implémente plusieurs tables différentes, certaines pour une utilisation par des applications clientes, d’autres pour une utilisation par des fournisseurs de services et d’autres pour une utilisation par les deux. La table d’état est unique en ce que MAPI fournit finalement la table, mais les lignes sont composées de contributions de tous les types de fournisseurs de services en plus de MAPI. 
  
L’illustration suivante illustre l’une des utilisations fréquentes d’un tableau dans MAPI : pour afficher le contenu d’un dossier. À droite se trouve un affichage de deux messages, comme cela peut apparaître dans une application cliente de messagerie classique. L’affichage contient quatre informations sur chaque message : l’expéditeur, le destinataire, l’objet et le texte du message. Chaque élément d’information correspond à une propriété du message.
  
Sur la gauche se trouve une vue de la table des matières qui inclut ces deux messages. Alors que la table des matières peut avoir dix lignes, car le dossier contient dix messages, chaque ligne contenant plus de trois colonnes, cette vue particulière est limitée à seulement deux lignes et trois colonnes.
  
Le tableau suivant montre les propriétés qui composent l’ensemble de colonnes pour l’affichage table.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nom de l’expéditeur  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Date et heure d’envoi du message  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Ligne d’objet du message  <br/> |
   
Notez que l’ensemble des propriétés affichées dans le message n’est pas le même que celui des colonnes affichées dans le tableau. L’implémenteur de la table, dans ce cas un fournisseur de magasin de messages, fournit un ensemble de colonnes par défaut dans un ordre par défaut. Le client peut modifier cet ensemble de colonnes, demander des colonnes supplémentaires ou rejeter celles par défaut et demander qu’elles soient ordonnées d’une manière spécifique. Le client peut également classer les lignes en les triant en fonction de la valeur d’une ou plusieurs colonnes.
  
**Utilisation d’un tableau pour afficher le contenu du dossier**
  
![Utilisation d’un tableau pour afficher le contenu du dossier](media/amapi_54.gif "Utilisation d’un tableau pour afficher le contenu du dossier")
  
Il existe deux interfaces pour l’utilisation des tables :
  
- [IMAPITable : IUnknown](imapitableiunknown.md) offre aux clients et aux fournisseurs de services une vue en lecture seule des données sous-jacentes de la table, ce qui leur permet d’afficher et de modifier uniquement la présentation. Plusieurs utilisateurs peuvent accéder aux mêmes données simultanément avec **IMAPITable**. **IMAPITable** est implémenté par MAPI et par les fournisseurs de services. 
    
- [ITableData : IUnknown](itabledataiunknown.md) donne aux clients et aux fournisseurs de services un accès en lecture/écriture aux données sous-jacentes de la table, ce qui leur permet d’apporter des modifications permanentes. **IMAPITable** est implémenté par MAPI et utilisé principalement par les fournisseurs de services qui y accèdent en appelant la fonction [CreateTable](createtable.md) . L’implémentation **ITableData** contient toutes les données de la table et toutes les restrictions associées en mémoire, ce qui la rend impropres à une utilisation avec des tables très volumineuses. Les restrictions composées et les opérations complexes telles que la catégorisation ne sont pas prises en charge. 
    
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI](mapi-concepts.md)

