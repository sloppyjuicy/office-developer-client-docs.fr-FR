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
ms.openlocfilehash: 7c3c4479cd401a163e34c819ecd44e86d1d01965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784723"
---
# <a name="mapi-tables"></a>Tables MAPI
  
**S’applique à**: Outlook 
  
Une table MAPI est un objet MAPI qui est utilisé pour afficher une collection de propriétés appartenant à d’autres objets MAPI d’un type particulier. Tables MAPI sont organisées dans un format de ligne et de colonne et chaque ligne représente un objet et chaque colonne représentant une propriété de l’objet. Une des propriétés généralement incluses dans chaque ligne est la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), un identificateur qui peut être utilisé pour ouvrir et modifier l’objet. 
  
Étant donné que les lignes contiennent des valeurs de propriété, extraire une ligne d’une table est similaire à un ensemble de propriétés directement à partir de l’objet qui représente la ligne. Les deux opérations entraîner l’extraction d’un tableau de valeurs de propriété. La principale différence réside dans la gestion de la durée des propriétés de chaîne et binaires. Inclus dans une table, de l’implémentation de certaines tableau tronque ces propriétés à 255 octets. Lorsque récupérées directement à partir de l’objet, la valeur complète est toujours disponible.
  
Les tableaux sont implémentés par les fournisseurs de magasins de messages et du carnet d’adresses et MAPI, en fonction du type de table et les objets qu’il contient. Un fournisseur de magasin de message implémente des dossiers et une table des matières pour chaque dossier qui consacrée des informations sur les messages dans le dossier. Un fournisseur de carnet d’adresses implémente des conteneurs de carnet d’adresses et une table de hiérarchie indiquant leur organisation. MAPI implémente différentes tables, certains pour une utilisation par les applications clientes, certains pour une utilisation par les fournisseurs de services et autres pour une utilisation par les deux. La table d’état est unique dans la mesure où MAPI fournit enfin le tableau, mais les lignes sont composés des contributions de tous les types de fournisseurs de services en plus de MAPI. 
  
L’illustration suivante montre l’une des utilisations d’une table fréquentes MAPI : pour afficher le contenu d’un dossier. Sur la droite est un affichage de deux messages comme peut apparaître dans une application client de messagerie par défaut. L’affichage contienne quatre éléments d’information sur chaque message : l’expéditeur, le destinataire, l’objet et le texte du message. Chaque élément d’information correspond à une propriété du message.
  
Sur la gauche est un affichage de la table de contenu qui inclut les deux messages. Que la table des matières peut avoir dix lignes, car le dossier a dix messages, chaque ligne contenant le nombre de plus de trois colonnes, cet affichage particulier est limité à deux lignes et trois colonnes.
  
Le tableau suivant présente les propriétés qui constituent la colonne définie pour la vue table.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nom de l’expéditeur  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Date et heure auxquelles le message a été envoyé.  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Objet du message  <br/> |
   
Notez que l’ensemble des propriétés affichées dans le message ne sont pas la même que l’ensemble des colonnes affichées dans le tableau. Implémentation de la table, en l’occurrence un message de fournisseur de magasins, fournit la valeur par défaut des colonnes dans un ordre par défaut. Le client peut modifier cet ensemble de colonnes, qui demande des colonnes supplémentaires ou du rejet des modèles par défaut et demander qu’ils classés de manière spécifique. Le client peut également commander les lignes, les trier en fonction de la valeur d’une ou plusieurs colonnes.
  
**Utilisation d’un tableau pour afficher le contenu du dossier**
  
![Utilisation d’un tableau pour afficher le contenu du dossier] (media/amapi_54.gif "Utilisation d’un tableau pour afficher le contenu du dossier")
  
Il existe deux interfaces pour l’utilisation des tableaux :
  
- [IMAPITable : IUnknown](imapitableiunknown.md) donne des clients et des fournisseurs de services une vue en lecture seule des données sous-jacentes de la table, de sorte qu’ils puissent afficher et modifier uniquement la présentation. Plusieurs utilisateurs peuvent accéder aux données même pendant le **IMAPITable**. **IMAPITable** est implémentée par MAPI et par les fournisseurs de services. 
    
- [ITableData : IUnknown](itabledataiunknown.md) permet aux clients et fournisseurs de services en lecture/écriture l’accès aux données de la table sous-jacente sorte qu’ils puissent apporter des modifications permanentes. **IMAPITable** est implémentée par MAPI et utilisé principalement par les fournisseurs de services qui ont accès en appelant la fonction [Create table](createtable.md) . L’implémentation de **ITableData** conserve toutes les données de la table et tout programme associé restrictions en mémoire, rendant inapproprié pour utilisent des tableaux de très grande taille. Restrictions composées et des opérations complexes, telles que la catégorisation sont non pris en charge. 
    
## <a name="see-also"></a>Voir aussi

- [Concepts MAPI (en anglais)](mapi-concepts.md)

