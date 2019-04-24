---
title: Tables MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 840c34a64cd0478be8f208799653b9916f50079d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355834"
---
# <a name="mapi-tables"></a>Tables MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table MAPI est un objet MAPI qui permet d'afficher une collection de propriétés appartenant à d'autres objets MAPI d'un type particulier. Les tables MAPI sont structurées dans un format de ligne et de colonne avec chaque ligne représentant un objet et chaque colonne représentant une propriété de l'objet. L'une des propriétés généralement incluses dans chaque ligne est la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), un identificateur qui peut être utilisé pour ouvrir et modifier l'objet. 
  
Étant donné que les lignes contiennent des valeurs de propriété, l'extraction d'une ligne d'une table revient à obtenir un ensemble de propriétés directement à partir de l'objet représenté par la ligne. Les deux opérations entraînent la récupération d'un tableau de valeurs de propriété. La principale différence réside dans la gestion de la chaîne longue et des propriétés binaires. Pour l'inclusion dans un tableau, certains implémenteurs de tableaux tronquent ces propriétés à 255 octets. Lorsqu'elle est récupérée directement à partir de l'objet, la valeur complète est toujours disponible.
  
Les tables sont implémentées par les fournisseurs de carnet d'adresses et de banque de messages et par MAPI, en fonction du type de table et des objets qu'elle contient. Un fournisseur de banque de messages implémente des dossiers et une table des matières pour chaque dossier qui inclut des informations sur les messages dans le dossier. Un fournisseur de carnet d'adresses implémente les conteneurs du carnet d'adresses et un tableau de hiérarchie qui affiche leur organisation. MAPI implémente différentes tables, certaines pour les applications clientes, certaines pour les fournisseurs de services et d'autres pour les deux. La table d'État est unique dans la situation où MAPI fournit finalement le tableau, mais les lignes sont constituées de contributions de tous les types de fournisseurs de services en plus de MAPI. 
  
L'illustration suivante montre l'une des utilisations fréquentes d'une table dans MAPI: pour afficher le contenu d'un dossier. À droite est un affichage de deux messages qui peut apparaître dans une application cliente de messagerie classique. L'affichage contient quatre informations sur chaque message: l'expéditeur, le destinataire, l'objet et le texte du message. Chaque information correspond à une propriété du message.
  
Sur la gauche figure une vue de la table des matières qui inclut ces deux messages. Alors que la table des matières peut comporter dix lignes, car le dossier comporte dix messages, chaque ligne contenant plus de trois colonnes, cet affichage particulier est limité à deux lignes et trois colonnes.
  
Le tableau suivant présente les propriétés qui composent le jeu de colonnes de l'affichage tableau.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nom de l'expéditeur  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Date et heure d'envoi du message  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Ligne d'objet du message  <br/> |
   
Notez que le jeu de propriétés affiché dans le message n'est pas le même que l'ensemble de colonnes affiché dans le tableau. L'implémenteur du tableau, dans ce cas un fournisseur de banque de messages, fournit un ensemble de colonnes par défaut dans un ordre par défaut. Le client peut modifier cet ensemble de colonnes, demander des colonnes supplémentaires ou rejeter les paramètres par défaut et demander à ce qu'ils soient classés d'une manière spécifique. Le client peut également trier les lignes, en les triant en fonction de la valeur d'une ou plusieurs colonnes.
  
**Utilisation d’un tableau pour afficher le contenu du dossier**
  
![Utilisation d'un tableau pour afficher le contenu d'un dossier] (media/amapi_54.gif "Utilisation d'un tableau pour afficher le contenu d'un dossier")
  
Il existe deux interfaces pour travailler avec des tableaux:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) donne aux clients et aux fournisseurs de services une vue en lecture seule des données sous-jacentes de la table, ce qui leur permet d'afficher et de modifier uniquement la présentation. Plusieurs utilisateurs peuvent accéder aux mêmes données simultanément avec la fonction **IMAPITable**. La propriété **IMAPITable** est implémentée par MAPI et par les fournisseurs de services. 
    
- [ITableData: IUnknown](itabledataiunknown.md) donne aux clients et aux fournisseurs de services un accès en lecture/écriture aux données sous-jacentes de la table, ce qui leur permet d'effectuer des modifications permanentes. La méthode **IMAPITable** est implémentée par MAPI et utilisée principalement par les fournisseurs de services qui y accèdent en appelant la fonction [CreateTable](createtable.md) . L'implémentation de **ITableData** contient toutes les données de la table et toutes les restrictions associées dans la mémoire, ce qui rend l'utilisation de tables très volumineuses. Les restrictions composées et les opérations complexes telles que la catégorisation ne sont pas prises en charge. 
    
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI](mapi-concepts.md)

